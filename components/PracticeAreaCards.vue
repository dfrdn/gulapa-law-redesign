<template>
  <div>
    <b-container fluid="lg">
      <b-row align-h="center" class="flex-wrap">
        <b-col
          v-for="practiceArea in allPracticeAreas"
          :key="practiceArea.description"
          class="practiceArea d-flex flex-column text-center px-4 mx-0 my-2 col-12 col-md-4"
        >
          <img class="img-fluid" :src="practiceArea.icon" :alt="practiceArea.description" />
          <h2>{{ practiceArea.description }}</h2>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      allPracticeAreas: [
        {
          icon: require('~/assets/images/practice-areas/corporate.svg'),
          description: 'General Corporate',
        },
        {
          icon: require('~/assets/images/practice-areas/structural.svg'),
          description: 'Infrastructure',
        },
        {
          icon: require('~/assets/images/practice-areas/government.svg'),
          description: 'Government Contracts',
        },
        {
          icon: require('~/assets/images/practice-areas/dispute.svg'),
          description: 'Dispute Resolution',
        },
        {
          icon: require('~/assets/images/practice-areas/tax.svg'),
          description: 'Tax',
        },
        {
          icon: require('~/assets/images/practice-areas/itech.svg'),
          description: 'I-tech & Intellectual Property',
        },
        {
          icon: require('~/assets/images/practice-areas/hrm.svg'),
          description: 'Human Resources & Immigration',
        },
        {
          icon: require('~/assets/images/practice-areas/fem.svg'),
          description: 'Fashion, Entertainment, & Media (FEM)',
        },
        {
          icon: require('~/assets/images/practice-areas/innovation.svg'),
          description: 'Innovation & Competition',
        },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
</style>
