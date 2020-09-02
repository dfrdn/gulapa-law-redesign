<template>
  <div>
    <b-container>
      <b-row class="p-3 p-lg-5 align-items-start">
        <b-col class="d-flex flex-column align-items-center">
          <h1 class="text-center p-0 mb-3">{{ info.title }}</h1>
          <img :src="getImage(info.slug)" :alt="`${info.slug} image`" class="img-fluid my-3" />
          <nuxt-content :document="info" />
        </b-col>
        <b-col id="list" cols="4" class="p-5">
          <practice-area-list :allPracticeAreas="allPracticeAreas" :active="info.title"></practice-area-list>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $content, params }) {
    const info = await $content(
      `practice-areas/${params.slug}` || 'index'
    ).fetch()

    const allPracticeAreas = await $content('practice-areas')
      .only(['title', 'slug'])
      .fetch()
    return { info, allPracticeAreas }
  },
  methods: {
    getImage(filename: String) {
      return require(`@/assets/images/practice-areas/${filename}.svg`)
    },
  },
})
</script>

<style scoped>
.nuxt-content-container {
  max-width: 800px;
}

#list {
  position: sticky;
  top: 10%;
}
</style>
