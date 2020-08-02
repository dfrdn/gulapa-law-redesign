<template>
  <div>
    <p class="pl-lg-5" :class="[variant]"><slot></slot></p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    variant: { type: String, default: 'accent' },
  },
})
</script>

<style lang="scss" scoped>
p {
  &.accent {
    color: white;
  }

  &.secondary {
    color: $secondary;
  }
}
</style>
