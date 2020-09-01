<template>
  <section id="practice-areas">
    <!-- <PracticeAreaCards /> -->
    <b-container>
      <b-row>
        <b-col class="d-flex flex-column">
          <PageTitle
            heading="Our Practice Areas"
            subheading="Different Clients, Different Needs"
            variant="secondary"
          />
        </b-col>
      </b-row>
      <b-row>
        <b-col
          v-for="practiceArea in allPracticeAreas"
          :key="practiceArea.description"
          class="d-flex flex-column justify-content-center align-items-center text-center mx-0 my-3 col-12 col-lg-4"
        >
          <practice-area-card
            :title="practiceArea.title"
            :description="practiceArea.description"
            :icon="getImage(practiceArea.slug)"
            :to="`/practice-areas/${practiceArea.slug}`"
          ></practice-area-card>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  async asyncData({ $content }) {
    const allPracticeAreas: {
      [key: string]: string | number
    }[] = await $content('practice-areas' || 'index').fetch()
    allPracticeAreas.sort((a, b) => (a.order as number) - (b.order as number))
    return { allPracticeAreas }
  },
  methods: {
    getImage(filename: String) {
      return require(`@/assets/images/practice-areas/${filename}.svg`)
    },
  },
})
</script>

<style></style>
