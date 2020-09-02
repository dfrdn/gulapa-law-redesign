<template>
  <nuxt-link :to="to">
    <div
      v-b-hover="handleHover"
      class="practiceArea d-flex flex-column align-items-center"
      :class="size"
    >
      <div v-if="isHovered" class="hovered text-left">
        <img :src="icon" alt="icon" height="30" />
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
      </div>
      <div v-else>
        <img :src="icon" :alt="title" height="80" />
        <h2>{{ title }}</h2>
      </div>
    </div>
  </nuxt-link>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    icon: { type: String, default: '' },
    description: { type: String, default: '' },
    title: { type: String, default: '' },
    size: { type: String, default: '' },
    to: { type: String, default: '/' },
  },
  data() {
    return {
      isHovered: false,
    }
  },
  methods: {
    handleHover(hovered: boolean) {
      this.isHovered = hovered
    },
  },
})
</script>

<style lang="scss" scoped>
.practiceArea {
  padding-top: 20px;
  width: 280px;
  height: 280px;
  border-radius: 10px;
  background: #fff;
  box-shadow: 3px 6px 10px rgba(0, 0, 0, 0.16);
  transition: 0.5s ease;

  img {
    margin-bottom: 40px;
  }
  h2 {
    width: 150px;
    font-size: 1.25rem;
    font-weight: 600;
  }

  &:hover {
    img {
      margin-bottom: 5px;
    }
    h2 {
      color: $accent;
    }
    p {
      color: white;
      overflow: hidden;
      font-size: 14px;
      max-width: 20ch;
    }

    background: $primary;
  }
}

a,
a:hover {
  text-decoration: none;
}

.sm {
  width: 230px;
  height: 230px;
}
</style>
