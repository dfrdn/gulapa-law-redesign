<template>
  <div>
    <b-container>
      <b-row class="p-3 p-lg-5 align-items-start">
        <b-col class="d-flex flex-column align-items-center">
          <h1 class="text-center p-0 mb-3">{{ info.name }}</h1>
          <p>
            <span class="mx-3"
              ><i class="fas fa-envelope mx-2"></i>{{ info.email }}</span
            >
            <span class="mx-3"
              ><i class="fas fa-phone mx-2"></i>{{ info.tel }}</span
            >
          </p>
          <img
            :src="getImage(info.slug)"
            :alt="`${info.slug} image`"
            class="img-fluid my-3"
          />
          <nuxt-content :document="info" />
        </b-col>
        <b-col id="list" cols="4" class="p-5">
          <lawyers-list :lawyers="lawyers" :active="info.name"></lawyers-list>
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

    const lawyers = await $content('lawyers').only(['name', 'slug']).fetch()
    return { info, lawyers }
  },
  methods: {
    getImage(filename: String) {
      return require(`@/assets/images/lawyers/${filename}.jpg`)
    },
  },
  transition(to, from) {
    if (to.name === from.name) return 'none'
    else return 'page'
  },
})
</script>

<style lang="scss" scoped>
.nuxt-content-container {
  max-width: 800px;
}

#list {
  position: sticky;
  top: 10%;
}
</style>
