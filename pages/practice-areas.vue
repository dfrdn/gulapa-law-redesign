<template>
  <section id="practice-areas">
    <!-- <PracticeAreaCards /> -->
    <b-container>
      <b-row>
        <b-col
          v-for="practiceArea in allPracticeAreas"
          :key="practiceArea.description"
          class="d-flex flex-column justify-content-center align-items-center text-center mx-0 my-3 col-12 col-lg-4"
        >
          <practice-area-card
            :title="practiceArea.title"
            :description="practiceArea.description"
            :icon="practiceArea.icon"
          ></practice-area-card>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script>
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      allPracticeAreas: [
        {
          icon: require('~/assets/images/practice-areas/corporate.svg'),
          title: 'General Corporate',
          description: 'General Corporate',
        },
        {
          icon: require('~/assets/images/practice-areas/structural.svg'),
          title: 'Infrastructure',
          description: 'Infrastructure',
        },
        {
          icon: require('~/assets/images/practice-areas/government.svg'),
          title: 'Government Contracts',
          description: 'Government Contracts',
        },
        {
          icon: require('~/assets/images/practice-areas/dispute.svg'),
          title: 'Dispute Resolution',
          description: 'Dispute Resolution',
        },
        {
          icon: require('~/assets/images/practice-areas/tax.svg'),
          title: 'Tax',
          description: 'Tax',
        },
        {
          icon: require('~/assets/images/practice-areas/itech.svg'),
          title: 'I-tech & Intellectual Property',
          description: 'I-tech & Intellectual Property',
        },
        {
          icon: require('~/assets/images/practice-areas/hrm.svg'),
          title: 'Human Resources & Immigration',
          description: 'Human Resources & Immigration',
        },
        {
          icon: require('~/assets/images/practice-areas/fem.svg'),
          title: 'Fashion, Entertainment, & Media (FEM)',
          description: 'Fashion, Entertainment, & Media (FEM)',
        },
        {
          icon: require('~/assets/images/practice-areas/innovation.svg'),
          title: 'Innovation & Competition',
          description: 'Innovation & Competition',
        },
        {
          icon: require('~/assets/images/practice-areas/asean.svg'),
          title: 'ASEAN Trade',
          description: 'ASEAN Trade',
        },
        {
          icon: require('~/assets/images/practice-areas/newyork.svg'),
          title: 'Doing Business in New York',
          description: 'Doing Business in New York',
        },
        {
          icon: require('~/assets/images/practice-areas/data-privacy.svg'),
          title: 'Data Privacy Act Compliance',
          description: 'Data Privacy Act Compliance',
        },
      ],
    }
  },
})
</script>

<style></style>
