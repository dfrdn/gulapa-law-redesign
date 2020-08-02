<template>
  <footer id="footer-wrap">
    <section id="pre-footer">
      <b-container>
        <b-row class="text-center">
          <b-col class="connect col-12 col-md col-lg-3">
            <h3 class="mb-4">Connect with Us</h3>
            <ul class="p-0">
              <li class="my-3">
                <img class="mr-2" src="~assets/images/mail.svg" alt="mail" />
                <span>glaw@gulapalaw.com</span>
              </li>
              <li class="my-3">
                <img class="mr-2" src="~assets/images/phone.svg" alt="phone" />
                <span>+63 2960 2845 to 47</span>
              </li>
            </ul>
          </b-col>
          <b-col class="address col-12 col-md col-lg-3">
            <h3 class="mb-4">Manila Address</h3>
            <b-row class="justify-content-center">
              <b-col class="col-auto">
                <img src="~assets/images/pin.svg" alt="pin" />
              </b-col>
              <b-col class="px-0 col-sm-4 col-md">
                <span>
                  G-Law (Gulapa Law Office)
                  Unit 12-A, 12th Floor, Marco Polo Ortigas Manila
                  Sapphire Road, Ortigas Center
                  1605 Pasig City
                </span>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section id="footer">
      <b-container>
        <b-row class="text-center py-3 justify-content-md-between align-items-center">
          <b-col class="col-12 col-md-auto mb-3 mb-md-0">
            <h6 class="g-law my-0">All Rights Reserved | Gulapa Law 2020</h6>
          </b-col>
          <b-col class="col-12 col-md-auto">
            <ul class="social-icons my-0">
              <li>
                <a href="https://www.facebook.com/Gulapa-Law-Office-156580428029762">
                  <img src="~/assets/images/social-icons/facebook.svg" alt="facebook" />
                </a>
              </li>
              <li>
                <a href="https://www.instagram.com/gulapa_law/">
                  <img src="~/assets/images/social-icons/twitter.svg" alt="twitter" />
                </a>
              </li>
              <li>
                <a href="https://twitter.com/gulapa_law">
                  <img src="~/assets/images/social-icons/instagram.svg" alt="instagram" />
                </a>
              </li>
              <li>
                <a href="https://www.linkedin.com/company/7602818">
                  <img src="~/assets/images/social-icons/linkedin.svg" alt="linkedin" />
                </a>
              </li>
            </ul>
          </b-col>
        </b-row>
      </b-container>
    </section>
  </footer>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
#pre-footer {
  margin-top: 50px;
  padding: 40px 0;
  background: $primary;

  h3 {
    font-size: 24px;
    font-weight: 600;
    color: $accent;
    text-transform: uppercase;
  }

  ul {
    list-style: none;
  }

  span {
    color: white;
  }
}

.g-law {
  color: $secondary;
}

.social-icons li {
  display: inline;
  margin-right: 20px;
}
</style>
