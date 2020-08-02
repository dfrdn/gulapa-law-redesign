<template>
  <section id="awards">
    <b-container>
      <b-row>
        <b-col class="d-flex flex-column">
          <PageTitle
            heading="Gains and Recognitions"
            subheading="We strive to be exceptional"
            variant="secondary"
          />
          <div class="text-container">
            <div class="award">
              <div class="headerBox">
                <h3>Asian Business Law Journal</h3>
              </div>
              <ul>
                <li>Top 100 Lawyers in the Philippines, Aris L. Gulapa (2018)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>Asian Legal Business Philippine Law Awards</h3>
              </div>
              <ul>
                <li>Rising Law Firm of the Year (winner) (2018)</li>
                <li>Boutique Law Firm of the Year (2016)</li>
                <li>Project Finance Deal of the Year, finalist (2016)</li>
                <li>Philippine Law Firm of the Year, nominee (2016)</li>
                <li>Rising Law Firm of the Year, finalist (2016)</li>
                <li>Construction Law Firm of the Year, finalist (2016)</li>
                <li>Young Lawyer of the Year, Aris Gulapa, finalist (2016)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>Asian Legal Business Southeast Asia Law Awards</h3>
              </div>
              <ul>
                <li>Asset & Corporate Finance Deal of the Year, nominee (2016)</li>
                <li>Boutique Law Firm of the Year, finalist (2016)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>International Financial Law Review</h3>
              </div>
              <ul>
                <li>Project Development & Project Finance, Notable Law Firm (2019)</li>
                <li>Financial and Corporate, Notable Firm in (a) M & A; (b) Project Finance; and (c) Restructuring & Insolvency (2017)</li>
                <li>Energy & Infrastructure Guide, Notable Law Firm (2016)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>Asialaw Profiles</h3>
              </div>
              <ul>
                <li>Construction & Real Estate (Recommended Law Firm); Projects & Infrastructure (Recommended Law Firm) (2019)</li>
                <li>Competition/Antitrust (Recommended Law Firm) (2017)</li>
                <li>Construction & Real Estate (Recommended Law Firm) (2017)</li>
                <li>Corporate/M&A (Recommended Law Firm) (2017)</li>
                <li>Projects & Infrastructure (Recommended Law Firm) (2017)</li>
                <li>Restructuring & Insolvency (Recommended Law Firm) (2017)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>Chambers & Partners Asia Pacific</h3>
              </div>
              <ul>
                <li>Projects, Energy & Infrastructure, Aris L. Gulapa, Band 3 (2019)</li>
                <li>Corporate/M&A, Aris Gulapa, Band 3 (2017; 2016)</li>
                <li>Projects, Energy & Infrastructure, Aris Gulapa, Up and Coming (2017; 2016)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>Chambers & Partners Global</h3>
              </div>
              <ul>
                <li>Corporate/Finance, Aris Gulapa, Band 3 (2017; 2016)</li>
                <li>Projects, Energy & Infrastructure, Aris Gulapa, Up and Coming (2017; 2016)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>The Legal500</h3>
              </div>
              <ul>
                <li>Real Estate & Construction (Tier 1); Projects & Infrastructure (Recommended Law Firm) (2018)</li>
                <li>Real Estate & Construction, Aris L. Gulapa (Leading Individual) (2018)</li>
                <li>Real Estate & Construction (Tier 1) (2017)</li>
                <li>Corporate/M&A (Recommended Law Firm) (2017)</li>
                <li>Projects & Infrastructure (Recommended Law Firm) (2017)</li>
                <li>Real Estate & Construction, Aris Gulapa, Leading Individual (2016)</li>
                <li>Projects & Infrastructure, Aris Gulapa, Recommended Individual (2016)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>Asian Legal Business Southeast Asia Law Awards</h3>
              </div>
              <ul>
                <li>Construction Law Firm of the Year, finalist (2017)</li>
                <li>Energy and Resources Law Firm of the Year, finalist (2017)</li>
                <li>Real Estate Law Firm of the Year, finalist (2017)</li>
                <li>Rising Law Firm of the Year, finalist (2017)</li>
                <li>Transactional Boutique Law Firm of the year, finalist (2017)</li>
                <li>Asset & Corporate Finance Deal of the Year for its new Philippine e-Passport System Project, nominee (2016)</li>
                <li>Boutique Law Firm of the Year, finalist (2016)</li>
              </ul>
            </div>

            <div class="award">
              <div class="headerBox">
                <h3>The In-House Community Counsels of the Year (Asian-Mena)</h3>
              </div>
              <ul>
                <li>Aris Gulapa, Commended External Counsel (2017)</li>
              </ul>
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.headerBox {
  padding: 5px 0 5px 15px;
  text-transform: uppercase;

  width: 100%;
  max-width: 1100px;
  width: 100%;
  text-align: left;
  background: transparent linear-gradient(180deg, white 0%, #fafafa 100%) 0% 0%;
  box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.16078);
  border-radius: 10px;

  h3 {
    font-size: 24px;
    font-weight: 600;
    color: $accent;
    margin: 0;
  }
}

.award {
  margin: 60px 0;

  ul {
    list-style: none;
    margin-top: 20px;

    li {
      margin-bottom: 10px;
    }
  }
}

.text-container {
  color: $secondary;
  font-size: 16px;
  //   max-width: 1100px;
}
</style>
