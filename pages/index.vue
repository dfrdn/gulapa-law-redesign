<template>
  <div id="index-page">
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
          </b-col>
        </b-row>
        <b-row>
          <b-col class="text-center">
            <g-button variant="primary" to="/contact">Consult Us</g-button>
            <b-button variant="outline-primary" href="#about"
              >Learn More</b-button
            >
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
          <b-col align-self="start" class="d-flex flex-column">
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
              <g-button variant="accent" :more="true" to="/about"
                >Learn More</g-button
              >
            </span>
          </b-col>
          <b-col class="text-center">
            <img class="img-fluid" src="~/assets/images/who-we-are.png" alt />
          </b-col>
        </b-row>
        <b-row>
          <b-col class="d-flex justify-content-center mt-5">
            <timeline />
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="practice-areas">
      <b-container>
        <b-row align-v="center">
          <b-col cols="12" lg="4" class="d-flex flex-column">
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
              <g-button variant="primary" :more="true" to="/practice-areas"
                >See all practice areas</g-button
              >
            </span>
          </b-col>
          <b-col>
            <b-row class="flex-nowrap flex-lg-wrap overflow-auto">
              <b-col
                v-for="practiceArea in allPracticeAreas"
                :key="practiceArea.description"
                class="d-flex flex-column justify-content-center align-items-center text-center mx-0 my-5 my-lg-3 col-auto col-lg-4"
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
        <b-row class="justify-content-center">
          <h2>Notable Projects</h2>
        </b-row>
        <b-row class="px-4 text-center">
          <b-card-group deck>
            <b-card
              img-src="~/assets/images/lrt.jpg"
              img-alt="Card image"
              img-top
            >
              <b-card-title>LRT 6 Project</b-card-title>
            </b-card>

            <b-card
              img-src="~/assets/images/clark-airport.jpg"
              img-alt="Card image"
              img-top
            >
              <b-card-title>Clark Airport</b-card-title>
            </b-card>

            <b-card
              img-src="~/assets/images/naia.jpg"
              img-alt="Card image"
              img-top
            >
              <b-card-title>NAIA Expansion</b-card-title>
            </b-card>
          </b-card-group>
        </b-row>
      </b-container>
    </section>
    <section id="lawyers">
      <b-container>
        <b-row cols="1" cols-lg="2" align-v="end">
          <b-col class="d-flex flex-column">
            <section-title
              heading="Our Lawyers"
              subheading="Led by two of the most outstanding counsels counsels in the field"
              variant="secondary"
            ></section-title>
            <div id="aris-profile" class="my-4">
              <nuxt-link to="/lawyers/aris">
                <button class="profile px-3 py-2 my-3">Aris L. Gulapa</button>
              </nuxt-link>
              <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem
                facilis nesciunt porro nihil! Alias itaque et libero corporis
                neque nihil nulla perferendis laboriosam consectetur? A ipsa
                veniam corrupti eius illo.
              </p>
              <b-row align-h="around">
                <b-col>
                  <i class="fas fa-envelope mx-3"></i>aris.gulapa@gulapalaw.com
                </b-col>
                <b-col> <i class="fas fa-phone"></i>numbernumber </b-col>
              </b-row>
            </div>
            <div id="charms-profile" class="my-4">
              <nuxt-link to="/lawyers/charms">
                <button class="profile px-3 py-2 my-3">Charmaine Haw</button>
              </nuxt-link>
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
            <g-button variant="primary" :more="true" to="/lawyers"
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
    <section id="awards">
      <b-container>
        <b-row class="justify-content-center">
          <h2>Gains and Recognitions</h2>
        </b-row>
        <b-row cols="1" cols-md="2" cols-lg="3">
          <b-col>
            <div
              class="award text-center d-flex flex-column align-items-center"
            >
              <img src="~/assets/images/award-home.svg" alt="awards" />
              <h3>
                RISING LAW FIRM
                <br />OF THE YEAR (WINNER)
              </h3>
              <h3>2018</h3>
              <p>
                Asian Legal Business
                <br />Philippine Law Awards
              </p>
            </div>
          </b-col>
          <b-col>
            <div
              class="award text-center d-flex flex-column align-items-center"
            >
              <img src="~/assets/images/award-home.svg" alt="awards" />
              <h3>TOP 100 LAWYERS IN THE PHILIPPINES, ARIS L. GULAPA</h3>
              <h3>2018</h3>
              <p>
                Asian Business
                <br />Law Journal
              </p>
            </div>
          </b-col>
          <b-col>
            <div
              class="award text-center d-flex flex-column align-items-center"
            >
              <img src="~/assets/images/award-home.svg" alt="awards" />
              <h3>REAL ESTATE & CONSTRUCTION (TIER 1)</h3>
              <h3>2018</h3>
              <p>
                The
                <br />Legal500
              </p>
            </div>
          </b-col>
        </b-row>
        <b-row class="justify-content-center">
          <g-button variant="accent" :more="true" to="/awards"
            >See all Gains and Recognitions</g-button
          >
        </b-row>
      </b-container>
    </section>
    <section id="contact-us">
      <b-container>
        <b-row class="px-4 text-center">
          <section-title
            heading="Get In Touch"
            subheading="Law is a complicated matter. Please fill out this quick form to help us help you."
            variant="secondary"
          ></section-title>
        </b-row>
        <b-row align-h="center" class="my-lg-3">
          <b-col cols="12" lg="8">
            <b-form-row class="mx-auto justify-content-center">
              <b-form-input class="my-2" placeholder="Name"></b-form-input>
              <b-form-input
                class="my-2"
                placeholder="Email Address"
              ></b-form-input>
              <b-form-textarea
                no-resize
                class="my-2"
                rows="4"
                placeholder="Message"
              ></b-form-textarea>
              <g-button variant="primary">Submit</g-button>
            </b-form-row>
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
          description:
            'The firm and its lawyers have extensive experience in corporate...',
        },
        {
          icon: require('~/assets/images/practice-areas/structural.svg'),
          title: 'Infrastructure',
          description:
            'This is the firm’s main specialization. Although recently...',
        },
        {
          icon: require('~/assets/images/practice-areas/government.svg'),
          title: 'Government Contracts',
          description:
            'We regularly advise private entities and government agencies...',
        },
        {
          icon: require('~/assets/images/practice-areas/dispute.svg'),
          title: 'Dispute Resolution',
          description:
            'The firm’s lawyers have extensive and significant experience...',
        },
        {
          icon: require('~/assets/images/practice-areas/tax.svg'),
          title: 'Tax',
          description:
            'The firm assists clients in achieving optimal tax structures...',
        },
        {
          icon: require('~/assets/images/practice-areas/asean.svg'),
          title: 'ASEAN Trade',
          description:
            'The firm regularly advises various companies from the Southeast...',
        },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
#index-page {
  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
}

@media (max-width: 991px) {
  .col span,
  .col .btn,
  .flex-column span {
    align-self: center;
  }
}

header,
section,
footer {
  padding: 100px 0;
  @media (max-width: 992px) {
    padding: 50px 0;
  }
}

#header {
  background: url('~assets/images/gulapa-mtg-room_img.png');
  // background-color: black;
  margin-top: -180px;
  padding-top: 280px;
  padding-bottom: 80px;

  @media (max-width: 992px) {
    padding-top: 180px;
    padding-bottom: 0;
  }

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
  padding: 0;
  background: $primary;

  @media (max-width: 992px) {
    padding: 50px 0;
  }
}

#about {
  background: $primary;
}

#practice-areas .row,
#practice-areas .row::-webkit-scrollbar {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}

#projects {
  background: $primary;
  h2 {
    color: white;
    font-size: 36px;
    font-weight: 600;
  }

  img {
    height: 200px;
    object-fit: cover;
  }
  h4 {
    font-size: 24px;
    font-weight: 600;
  }

  .card {
    margin-top: 60px;
    border-color: $accent;
  }
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
  .btn {
    margin-top: 80px;
  }
  h2 {
    color: white;
    font-size: 36px;
    font-weight: 600;
  }
  .award {
    margin-top: 100px;
    position: relative;

    img {
      position: absolute;
      bottom: 110px;
    }
    h3 {
      width: 100%;
      max-width: 265px;
      font-size: 24px;
      font-weight: 600;
      color: $accent;
    }
    p {
      margin-top: 30px;
      color: white;
    }
  }
}

#contact-us {
  .form-row {
    width: 100%;
    max-width: 800px;
    .btn {
      width: 100%;
    }
  }
}
</style>
