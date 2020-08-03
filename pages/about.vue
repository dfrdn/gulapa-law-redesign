<template>
  <section id="about-us">
    <b-container class="container">
      <b-row>
        <b-col class="d-flex flex-column">
          <PageTitle
            heading="Who We Are"
            subheading="Innovate, Achieve, Excel"
            variant="secondary"
          />
          <div class="text-container align-self-center">
            <p>
              Gulapa Law was established by Aris L. Gulapa in September 2015
              after he left a Makati-based firm where he was a partner for four
              years. Before this, Aris was an associate in Anderson Mori &
              Tomotsune (Tokyo, ‎2008-2010); Kelvin Chia Partnership (Singapore
              and Vietnam, ‎2006-2008); and SyCip Salazar Hernandez & Gatmaitan
              ‎(2003-2006).
            </p>
            <p>
              In February 2017, the firm became the first Philippine-based law
              firm to establish an office in New York City through its
              affiliate, Gulapa & Baclay LLP. Earlier in 2017 as well, the firm
              sought to expand its capabilities, particularly by developing its
              litigation practice.
            </p>
            <p>
              In June 2018, Gulapa Law established a representative office in
              San Francisco to liaise with its US West Coast-based clients with
              Philippine bound legal concerns.
            </p>
            <p>
              With a view to harnessing its lawyers’ talents and tapping into
              global markets, the firm actively rotates its lawyers in its New
              York and San Francisco office for training and capacity building.
            </p>
            <p>
              Gulapa Law continues to expand globally, transcending borders and
              servicing more international clients, in line with its vision to
              continuously innovate, achieve and excel.
            </p>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  scrollToTop: true,
})
</script>

<style lang="scss" scoped>
.text-container {
  color: $secondary;
  font-size: 16px;
  max-width: 1100px;
}
</style>
