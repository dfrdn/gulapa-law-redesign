<template>
  <section id="lawyers">
    <b-container fluid="lg">
      <b-row cols="1" cols-md="3" cols-lg="4" align-h="center" align-v="stetch">
        <b-col v-for="lawyer in lawyers" :key="lawyer.name">
          <lawyer-card
            :image="lawyer.img"
            :name="lawyer.name"
            :email="lawyer.email"
          >
          </lawyer-card>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script>
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      lawyers: [
        {
          img: require('~/assets/images/lawyers/1-Melissa.jpg'),
          name: 'Melissa Chavez',
          email: 'melissa.chavez@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/2-Angel.jpg'),
          name: 'Angel Machuca',
          email: 'angelmachuca@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/3-Shwaid.jpg'),
          name: 'Al-Shwaid Ismael',
          email: 'alshwaid.ismael@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/4-Yas.jpg'),
          name: 'Yas Sanchez',
          email: 'yas.sanchez@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/5-Caloy.jpg'),
          name: 'Caloy Cajucom',
          email: 'caloy.cajucom@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/6-Aileen.jpg'),
          name: 'Aileen Sanguir',
          email: 'aileen.sanguir@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/7-Dake.jpg'),
          name: 'Dake Mandocdoc',
          email: 'dake.mandocdoc@gulapalaw.com',
        },
        {
          img: require('~/assets/images/lawyers/8-Phil.jpg'),
          name: 'Phil Recentes',
          email: 'phil.@gulapalaw.com',
        },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
.nuxt-link:hover {
  text-decoration: none;
}
</style>
