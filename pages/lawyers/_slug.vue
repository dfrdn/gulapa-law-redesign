<template>
  <div>
    <b-container>
      <b-row>
        <b-col>
          <nuxt-content :document="info" class="m-5 p-5" />
        </b-col>
      </b-row>
    </b-container>
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
