<template>
  <div>
    <b-container fluid="lg">
      <b-row align-h="center" class="flex-wrap">
        <b-col
          v-for="lawyer in allLawyers"
          :key="lawyer.name"
          class="lawyer d-flex flex-column text-center px-2 mx-0 my-2 col-12 col-md-3"
        >
          <img class="img-fluid" :src="lawyer.img" :alt="lawyer.name" />
          <div class="nameCard d-flex flex-column align-items-center">
            <h2>{{ lawyer.name }}</h2>
            <p>{{ lawyer.email }}</p>
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
      allLawyers: [
        {
          img: require('~/assets/images/lawyers/1-Melissa.jpg'),
          name: 'Melissa Chavez',
          email: 'melissa.chavez@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/2-Angel.jpg'),
          name: 'Angel',
          email: '@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/3-Shwaid.jpg'),
          name: 'Shwaid',
          email: '@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/4-Yas.jpg'),
          name: 'Yas',
          email: '@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/1-Melissa.jpg'),
          name: 'Melissa Chavez',
          email: 'melissa.chavez@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/2-Angel.jpg'),
          name: 'Angel',
          email: '@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/3-Shwaid.jpg'),
          name: 'Shwaid',
          email: '@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/4-Yas.jpg'),
          name: 'Yas',
          email: '@gulapalaw.com',
        },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
.lawyer img {
  object-fit: cover;
  border-radius: 10px 10px 0 0;
}

.nameCard {
  background: $primary;
  border-radius: 0 0 10px 10px;
  box-shadow: 0px 3px 6px 0px #0000000f;

  h2 {
    color: $accent;
    text-transform: uppercase;
    font-style: normal;
    font-weight: 400;
    font-size: 1.25rem;
  }

  p {
    color: var(--white);
    font-style: normal;
    font-weight: 400;
    font-size: 0.875rem;
  }
}
</style>
