<template>
  <div class="my-3">
    <nuxt-link :to="to">
      <b-card
        class="justify-content-between"
        img-top
        :img-src="image"
        :title="name"
      ></b-card>
    </nuxt-link>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    image: { type: String, default: '' },
    name: { type: String, default: '' },
    email: { type: String, default: '' },
    to: { type: String, default: '/' },
  },
  data() {
    return {
      isHovered: false,
    }
  },
})
</script>

<style lang="scss" scoped>
a,
a:hover {
  text-decoration: none;
}

.card {
  transition: 0.5s ease;
}
.card:hover {
  box-shadow: 0px 3px 6px 5px #0000002f;
}

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
