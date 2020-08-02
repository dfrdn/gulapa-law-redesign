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
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat
              eligendi consectetur voluptatum, laborum ea harum quidem amet.
            </p>
            <button class="btn btn-primary">Consult Now</button>
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
      <SectionTitle />
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
.container-fluid {
  // min-height: 100vh;
}

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
  }

  hr {
    border: 0;
    border-top: 3px solid $primary;
  }
}

#featured {
  scroll-snap-align: start;
  transform: translateY(-50%);
  padding: 0;
  // background: $primary;
}
</style>
