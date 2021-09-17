<template>
  <q-page class="container q-pa-lg">
    <h1>Posts</h1>
    <div class="row q-gutter-md justify-around">
      <div class="col-3" v-for="(post, index) in posts" :key="index">
        <q-card class="my-card" flat bordered>
          <q-img
            :src="post.jetpack_featured_media_url"
          />
          <q-card-section>
            <div class="text-overline text-orange-9">Overline</div>
            <div class="text-h5 q-mt-sm q-mb-xs">{{post.title.rendered}}</div>
            <div class="text-caption text-grey">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et
              dolore magna aliqua.
            </div>
          </q-card-section>

          <q-card-actions>
            <q-btn flat color="dark" label="Share"/>
            <q-btn flat color="primary" label="Book"/>

            <q-space/>

            <q-btn
              color="grey"
              round
              flat
              dense
              :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
              @click="expanded = !expanded"
            />
          </q-card-actions>

          <q-slide-transition>
            <div v-show="expanded">
              <q-separator/>
              <q-card-section class="text-subitle2">
                {{ lorem }}
              </q-card-section>
            </div>
          </q-slide-transition>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script>
/* eslint-disable */
import { ref } from 'vue'
export default {
  name: "Post",
  data() {
    return {
      posts: [],
      expanded: ref(false),
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  },
  mounted() {
    this.getPosts();
  },
  methods: {
    getPosts() {
      this.$q.loading.show({
        delay: 400 //ms
      });
      //this.$axios('https://josemalcher.net/wp-json/wp/v2/posts')
      this.$axios.get('https://viladosilicio.com.br/wp-json/wp/v2/posts')
        .then((res) => {
          this.posts = res.data
          this.$q.loading.hide();
          console.log('POSTS', res.data);
        })
        .catch((err) => {
          this.$q.loading.hide();
          console.log(err);
        })
    }
  }
}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 350px
</style>
