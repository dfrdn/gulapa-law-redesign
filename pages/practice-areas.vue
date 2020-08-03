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
          description:
            'The firm and its lawyers have extensive experience in corporate and commercial...',
        },
        {
          icon: require('~/assets/images/practice-areas/structural.svg'),
          title: 'Infrastructure',
          description:
            'This is the firm’s main specialization. Although recently established...',
        },
        {
          icon: require('~/assets/images/practice-areas/government.svg'),
          title: 'Government Contracts',
          description:
            'We regularly advise private entities and government agencies on procurement...',
        },
        {
          icon: require('~/assets/images/practice-areas/dispute.svg'),
          title: 'Dispute Resolution',
          description:
            'The firm’s lawyers have extensive and significant experience in domestic...',
        },
        {
          icon: require('~/assets/images/practice-areas/tax.svg'),
          title: 'Tax',
          description:
            'The firm assists clients in achieving optimal tax structures. We synthesize local...',
        },
        {
          icon: require('~/assets/images/practice-areas/itech.svg'),
          title: 'I-tech & Intellectual Property',
          description:
            'The firm’s active involvement in one of the biggest government projects has resulted...',
        },
        {
          icon: require('~/assets/images/practice-areas/hrm.svg'),
          title: 'Human Resources & Immigration',
          description:
            'The firm provides legal advice on all matters relating to human resource management...',
        },
        {
          icon: require('~/assets/images/practice-areas/fem.svg'),
          title: 'Fashion, Entertainment, & Media (FEM)',
          description:
            ' This is an emerging practice area in New York and Tokyo, which is gradually penetrating...',
        },
        {
          icon: require('~/assets/images/practice-areas/innovation.svg'),
          title: 'Innovation & Competition',
          description:
            'Competition law is an area that has not been tested before Philippine courts...',
        },
        {
          icon: require('~/assets/images/practice-areas/asean.svg'),
          title: 'ASEAN Trade',
          description:
            'The firm regularly advises various companies from the Southeast Asian region...',
        },
        {
          icon: require('~/assets/images/practice-areas/newyork.svg'),
          title: 'Doing Business in New York',
          description:
            'Gulapa & Baclay LLP is the New York affiliate of Gulapa Law, a law firm...',
        },
        {
          icon: require('~/assets/images/practice-areas/data-privacy.svg'),
          title: 'Data Privacy Act Compliance',
          description:
            'The firm regularly advises various local and international PIC/PIPs on compliance...',
        },
      ],
    }
  },
})
</script>

<style>
.practiceArea:hover p {
  height: 120px;
  text-overflow: ellipsis;
  white-space: wrap;
}
</style>
