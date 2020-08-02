<template>
  <b-button class="px-4" :class="[variant, more]">
    <slot></slot>
    <span v-if="more" class="mx-2">
      <img
        src="~assets/images/ionic-ios-arrow-dropright-circle.svg"
        alt="arrow more"
        height="15px"
      />
    </span>
  </b-button>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    variant: { type: String, default: 'accent' },
    more: { type: Boolean, default: false },
  },
})
</script>

<style lang="scss" scoped>
button {
  &.primary {
    background-color: $primary;
  }
  &.clear {
    background-color: transparent;
  }
  &.accent {
    background-color: $accent;
    border-color: $accent;
  }
}
</style>
