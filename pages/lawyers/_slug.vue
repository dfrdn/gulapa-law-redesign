<template>
  <div>
    <b-container>
      <b-row>
        <b-col class="d-flex flex-column align-items-center p-3 p-lg-5">
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
  methods: {
    getImage(filename: String) {
      return require(`@/assets/images/lawyers/${filename}.jpg`)
    },
  },
})
</script>

<style lang="scss" scoped>
.nuxt-content-container {
  max-width: 800px;
}
</style>
