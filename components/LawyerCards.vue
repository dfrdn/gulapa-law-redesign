<template>
  <div>
    <b-container fluid="lg">
      <b-row align-h="center" class="flex-wrap">
        <b-col
          v-for="lawyer in AllLawyers"
          :key="lawyer.name"
          class="lawyer d-flex flex-column text-center px-2 mx-0 my-2 col col-lg-3"
        >
          <img class="img-fluid" :src="lawyer.img" :alt="lawyer.name" />
          <div class="nameCard">
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
      AllLawyers: [
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
.nameCard {
  background: $primary;
}

.nameCard h2 {
  color: $accent;
}

.nameCard p {
  color: var(--white);
}
</style>
