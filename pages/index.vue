<template>
  <div id="page">
    <header id="header">
      <b-container fluid>
        <b-row align-h="center" align-v="center">
          <b-col class="mx-2 px-0">
            <hr />
          </b-col>
          <b-col class="col-auto text-center mx-2 px-0">
            <h1>Innovate, Achieve, and Excel with Us</h1>
          </b-col>
          <b-col class="mx-2 px-0">
            <hr />
          </b-col>
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
            <img class="img-fluid" src="~assets/images/header_img.png" alt />
          </b-col>
        </b-row>
      </b-container>
    </header>
    <section id="featured">
      <FeaturedCards />
    </section>
    <section id="about">
      <b-container>
        <b-row cols="1" cols-lg="2" align-v="start">
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
            <span class="pl-lg-5">
              <g-button variant="accent" :more="true">Learn More</g-button>
            </span>
          </b-col>
          <b-col>
            <img class="img-fluid" src="~/assets/images/who-we-are.png" alt />
          </b-col>
        </b-row>
        <b-row>
          <b-col>
            <timeline />
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="practice-areas">
      <b-container>
        <b-row align-v="center">
          <b-col cols="12" lg="4">
            <section-title
              heading="What We Do"
              subheading="Our Practice Areas"
              variant="secondary"
            />
            <section-details variant="secondary">
              Gulapa Law is dedicated in serving different clients across vast
              varieties of practice areas.
            </section-details>
            <span class="pl-lg-5">
              <g-button variant="primary" :more="true"
                >See all practice areas</g-button
              >
            </span>
          </b-col>
          <b-col>
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
                  size="sm"
                ></practice-area-card>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="projects">
      <b-container>
        <b-row>
          <b-row>Projects</b-row>
        </b-row>
      </b-container>
    </section>
    <section id="lawyers">
      <b-container>
        <b-row align-v="end">
          <b-col>
            <section-title
              heading="Our Lawyers"
              subheading="Led by two of the most outstanding lawyers in the field"
              variant="secondary"
            ></section-title>
            <div id="aris-profile" class="my-4">
              <nuxt-link to="/"
                ><button class="profile px-3 py-2 my-3">
                  Aris L. Gulapa
                </button></nuxt-link
              >
              <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem
                facilis nesciunt porro nihil! Alias itaque et libero corporis
                neque nihil nulla perferendis laboriosam consectetur? A ipsa
                veniam corrupti eius illo.
              </p>
              <b-row align-h="around">
                <b-col
                  ><i class="fas fa-envelope mx-3"></i
                  >aris.gulapa@gulapalaw.com</b-col
                >
                <b-col><i class="fas fa-phone"></i>numbernumber</b-col>
              </b-row>
            </div>
            <div id="charms-profile" class="my-4">
              <nuxt-link to="/"
                ><button class="profile px-3 py-2 my-3">
                  Charmaine Haw
                </button></nuxt-link
              >
              <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem
                facilis nesciunt porro nihil! Alias itaque et libero corporis
                neque nihil nulla perferendis laboriosam consectetur? A ipsa
                veniam corrupti eius illo.
              </p>
              <b-row align-h="around">
                <b-col>charms.haw@gulapalaw.com</b-col>
                <b-col>numbernumber</b-col>
              </b-row>
            </div>
            <g-button variant="primary" :more="true"
              >See all our lawyers</g-button
            >
          </b-col>
          <b-col>
            <img
              src="~assets/images/aris-landing_img.png"
              alt="Aris Gulapa"
              class="img-fluid profile"
            />
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="awards">awards</section>
    <section id="contact-us">
      <b-container>
        <b-row>
          <b-col cols="12" lg="8">
            <section-title
              heading="Get In Touch"
              subheading="Law is a complicated matter. Please fill out this quick form to help us help you."
              variant="secondary"
            ></section-title>
            <b-row-form>
              <b-form-input class="my-2" placeholder="Name"></b-form-input>
              <b-form-input
                class="my-2"
                placeholder="Email Address"
              ></b-form-input>
              <b-form-textarea
                no-resize=""
                class="my-2"
                rows="4"
                placeholder="Message"
              ></b-form-textarea>
              <g-button variant="primary">Submit</g-button>
            </b-row-form>
          </b-col>
          <b-col cols="12" lg="4">
            <div id="contacts">
              <h4>Connect with us</h4>
              <p><i class="fas fa-envelope mx-2"></i>glaw@gulapalaw.com</p>
              <p><i class="fas fa-phone mx-2"></i>+632 7960 2845 to 47</p>
            </div>
            <div id="address">
              <h4>Manila Address</h4>
              <p>addres</p>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </section>
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
          icon: require('~/assets/images/practice-areas/newyork.svg'),
          title: 'Doing Business in New York',
          description: 'Doing Business in New York',
        },
      ],
    }
  },
})
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

#projects {
  background: $primary;
}

#lawyers {
  button.profile {
    text-transform: uppercase;
    color: $primary;
    border: none;
    outline: none;
    width: 100%;
    text-align: left;
    background: transparent linear-gradient(180deg, white 0%, #fafafa 100%) 0%
      0%;
    box-shadow: 0px 3px 6px #00000029;
    border-radius: 10px;
  }
}

#awards {
  background: $primary;
}
</style>
