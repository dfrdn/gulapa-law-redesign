<template>
  <div id="pageTitle" class="my-5 text-center">
    <h3 :class="[variant]">{{ heading }}</h3>
    <hr class="my-0 py-0" :class="[variant]" />
    <h2 :class="[variant]">{{ subheading }}</h2>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    heading: { type: String, default: 'Heading', required: true },
    subheading: { type: String, default: '' },
    variant: { type: String, default: 'accent' },
  },
})
</script>

<style lang="scss" scoped>
h3 {
  text-transform: uppercase;
  font-size: 20px;
}

hr {
  border: 0;

  &.accent {
    border-top: 3px solid $secondary;
  }
  &.secondary {
    border-top: 3px solid $accent;
  }
}

h2 {
  font-size: 36px;
  font-weight: 600;
  text-transform: uppercase;
}
.accent {
  color: white;
}

.secondary {
  color: $primary;
}

@media (max-width: 992px) {
  h3,
  h2 {
    text-align: center;
  }
}
</style>
