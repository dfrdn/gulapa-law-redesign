<template>
  <div id="page">
    <header id="header">
      <b-container fluid>
        <b-row align-h="center" align-v="center">
          <b-col class="mx-2 px-0"><hr /></b-col>
          <b-col class="col-auto text-center mx-2 px-0">
            <h1>Innovate, Achieve, and Excel with Us</h1>
          </b-col>
          <b-col class="mx-2 px-0"><hr /></b-col>
        </b-row>
        <b-row>
          <b-col class="text-center">
            <p class="mx-auto">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat
              eligendi consectetur voluptatum, laborum ea harum quidem amet.
            </p>
            <g-button variant="primary">Consult Now</g-button>
            <button class="btn btn-outline-primary">Learn More</button>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="text-center">
            <img class="img-fluid" src="~assets/images/header_img.png" alt="" />
          </b-col>
        </b-row>
      </b-container>
    </header>
    <section id="featured">
      <FeaturedCards />
    </section>
    <section id="about">
      <b-container>
        <b-row align-v="start">
          <b-col align-self="start">
            <section-title heading="Who We Are" subheading="blabla" />
            <section-details>
              Gulapa Law was established by Aris L. Gulapa in September 2015
              after he left a Makati-based firm where he was a partner for four
              years. Before this, Aris was an associate in Anderson Mori &
              Tomotsune (Tokyo, ‎2008-2010); Kelvin Chia Partnership (Singapore
              and Vietnam, ‎2006-2008); and SyCip Salazar Hernandez & Gatmaitan
              ‎(2003-2006).
            </section-details>
            <span class="pl-lg-5"
              ><g-button variant="accent" :more="true"
                >Learn More</g-button
              ></span
            >
          </b-col>
          <b-col>
            <img
              class="img-fluid"
              src="~/assets/images/who-we-are.png"
              alt=""
            />
          </b-col>
        </b-row>
        <b-row>
          <b-col>
            <timeline />
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="practice-areas">practice areas</section>
    <section id="lawyers">lawyers</section>
    <section id="awards">awards</section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
#page {
  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
}

header,
section,
footer {
  padding: 100px 0;
}

#header {
  background: url('~assets/images/gulapa-mtg-room_img.png');
  margin-top: -180px;
  padding-top: 280px;

  background-size: auto 100%;
  background-repeat: no-repeat;
  scroll-snap-align: start;

  h1 {
    color: $primary;
    font-weight: 600;
  }

  hr {
    border: 0;
    border-top: 3px solid $primary;
  }

  p {
    color: #544c4c;
    font-size: 24px;
    max-width: 756px;
    // line-height: 30px;
  }
}

#featured {
  scroll-snap-align: start;
  // transform: translateY(-50%);
  padding: 0;
  background: $primary;

  @media (max-width: 992px) {
    padding: 100px 0;
  }
}

#about {
  background: $primary;
}
</style>
