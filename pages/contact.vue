<template>
  <section id="contact">
    <b-container class="container">
      <b-row>
        <b-col class="d-flex flex-column">
          <PageTitle
            heading="Get In Touch"
            subheading="Law is a complicated matter. Please fill out this quick form to help us help you."
            variant="secondary"
          />
        </b-col>
      </b-row>
      <b-row>
        <b-col>
          <b-form-row class="mx-auto justify-content-center">
            <b-form-input class="my-2" placeholder="Name"></b-form-input>
            <b-form-input class="my-2" placeholder="Email Address"></b-form-input>
            <b-form-textarea no-resize class="my-2" rows="4" placeholder="Message"></b-form-textarea>
            <g-button variant="primary">Submit</g-button>
          </b-form-row>
        </b-col>
      </b-row>
      <b-row>
        <div class="branch text-center">
          <h2>Manila Office</h2>
          <p>
            G-Law (Gulapa Law Office)
            <br />Unit 12-A, 12th Floor, Marco Polo Ortigas Manila
            <br />Sapphire Road, Ortigas Center
            <br />1605 Pasig City
          </p>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3861.2043849910665!2d121.0612529143691!3d14.587426581311298!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3397c810bdc60c3d%3A0x81c2b2cef364f4a6!2sMarco+Polo+Ortigas+Manila!5e0!3m2!1sen!2sph!4v1456922392250"
            height="300"
            frameborder="0"
            allowfullscreen
          ></iframe>
        </div>
      </b-row>
      <b-row>
        <div class="branch text-center">
          <h2>NEW YORK Office</h2>
          <p>
            1115 Broadway
            <br />(25th and Broadway)
            <br />near Madison Square Park
          </p>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3022.8615433012733!2d-73.99185584989148!3d40.743072043551116!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c259a4415ae31f%3A0x43ba72cced8ab9cd!2s1115+Broadway%2C+New+York%2C+NY+10010%2C+USA!5e0!3m2!1sen!2sph!4v1487078187026"
            height="300"
            frameborder="0"
            allowfullscreen
          ></iframe>
        </div>
      </b-row>
      <b-row>
        <div class="branch text-center">
          <h2>SAN FRANCISCO OFFICE</h2>
          <p>
            2/F 95 3rd and Mission Sts.
            <br />San Francisco, CA
            <br />94103 USA
          </p>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3153.1453723601717!2d-122.40439098468207!3d37.786632779757305!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80858087fb354153%3A0xef4c7d3de9b559c5!2s95+3rd+St%2C+San+Francisco%2C+CA+94103%2C+USA!5e0!3m2!1sen!2sph!4v1557731092401!5m2!1sen!2sph"
            height="350px"
            frameborder="0"
            allowfullscreen
          ></iframe>
        </div>
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
#contact {
  .form-row {
    width: 100%;
    max-width: 800px;
    .btn {
      width: 100%;
    }
  }
}

.branch {
  margin-top: 50px;
  padding: 20px;
  background: transparent linear-gradient(180deg, white 0%, #fafafa 100%) 0% 0%;
  width: 100%;
  box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.16078);
  border-radius: 10px;
  h2 {
    font-size: 24px;
    text-transform: uppercase;
    font-weight: 600;
  }
  p {
    color: $secondary;
  }
  iframe {
    width: 100%;
    border: 0;
  }
}
</style>
