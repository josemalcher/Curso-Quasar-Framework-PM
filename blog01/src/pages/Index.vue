<template>
  <q-page>
<!--    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    >-->
    <div class="q-pa-sm border-black">q-pa-sm</div>
    <div class="q-ml-xl q-mr-xl q-mt-xl border-black">q-ml-xl</div>
    <div class="q-ml-sm q-mr-sm q-mt-sm border-black">q-ml-sm</div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageIndex'
})
</script>

<style scoped>
.border-black {
  border: 1px solid black;
}
</style>
