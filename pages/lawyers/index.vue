<template>
  <section id="lawyers">
    <b-container fluid="lg">
      <b-row>
        <b-col class="d-flex flex-column">
          <PageTitle
            heading="Our Team"
            subheading="Brilliant and Prestigious Lawyers"
            variant="secondary"
          />
        </b-col>
      </b-row>
      <b-row cols="1" cols-md="3" cols-lg="4" align-h="center" align-v="stretch">
        <b-col v-for="lawyer in lawyers" :key="lawyer.name">
          <lawyer-card
            :image="getImage(lawyer.slug)"
            :name="lawyer.name"
            :email="lawyer.email"
            :to="`/lawyers/${lawyer.slug}`"
          ></lawyer-card>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  async asyncData({ $content }) {
    const lawyers = await $content('lawyers' || 'index').fetch()
    return { lawyers }
  },
  methods: {
    getImage(filename: String) {
      return require(`@/assets/images/lawyers/${filename}.jpg`)
    },
  },
})
</script>

<style lang="scss" scoped>
.nuxt-link:hover {
  text-decoration: none;
}
</style>
