<template>
  <b-button class="px-4" :class="[variant, more]" :to="to">
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
    to: { type: String, default: '/' },
  },
})
</script>

<style lang="scss" scoped>
$primary-hover: #192650;
$accent-hover: #d8a517;

a {
  &.primary {
    background-color: $primary;
    &:hover,
    &:focus,
    &:active {
      background-color: $primary-hover !important;
    }
  }
  &.clear {
    border: $primary;
    background-color: transparent;
  }
  &.accent {
    background-color: $accent;
    border-color: $accent;
    &:hover,
    &:focus,
    &:active {
      background-color: $accent-hover !important;
      border-color: $accent-hover;
    }
  }
}
</style>
