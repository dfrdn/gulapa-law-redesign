<template>
  <div>
    <nuxt-content :document="info" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $content, params }) {
    const info = await $content(`lawyers/${params.slug}` || 'index').fetch()
    return { info }
  },
})
</script>

<style scoped></style>
