<template>
  <div>
    <b-container fluid="lg">
      <b-row align-h="center" class="flex-wrap">
        <b-col
          v-for="practiceArea in allPracticeAreas"
          :key="practiceArea.description"
          class="d-flex flex-column justify-content-center align-items-center text-center mx-0 my-3 col-12 col-lg-4"
        >
          <div
            v-b-hover="handleHover"
            class="practiceArea d-flex flex-column align-items-center"
          >
            <h2 v-if="practiceArea.isHovered">HOVER</h2>
            <div v-else>
              <img
                :src="practiceArea.icon"
                :alt="practiceArea.description"
                height="80"
              />
              <h2>{{ practiceArea.description }}</h2>
            </div>
          </div>
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
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/structural.svg'),
          description: 'Infrastructure',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/government.svg'),
          description: 'Government Contracts',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/dispute.svg'),
          description: 'Dispute Resolution',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/tax.svg'),
          description: 'Tax',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/itech.svg'),
          description: 'I-tech & Intellectual Property',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/hrm.svg'),
          description: 'Human Resources & Immigration',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/fem.svg'),
          description: 'Fashion, Entertainment, & Media (FEM)',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/innovation.svg'),
          description: 'Innovation & Competition',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/asean.svg'),
          description: 'ASEAN Trade',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/newyork.svg'),
          description: 'Doing Business in New York',
          isHovered: false,
        },
        {
          icon: require('~/assets/images/practice-areas/data-privacy.svg'),
          description: 'Data Privacy Act Compliance',
          isHovered: false,
        },
      ],
      isHovered: false,
    }
  },
  methods: {
    handleHover(hovered) {
      this.isHovered = hovered
    },
  },
})
</script>

<style lang="scss" scoped>
.practiceArea {
  padding-top: 50px;
  width: 100%;
  height: 280px;
  border-radius: 10px;
  background: #fff;
  box-shadow: 3px 6px 10px rgba(0, 0, 0, 0.16);

  img {
    margin-bottom: 40px;
  }
  h2 {
    width: 150px;
    font-size: 1.25rem;
    font-weight: 600;
  }
}

// .practiceArea:hover {
//   background: $primary;
// }
</style>
