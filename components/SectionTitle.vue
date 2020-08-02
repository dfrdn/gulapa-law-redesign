<template>
  <div class="mb-lg-0 mb-5">
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
  data() {
    return {
      position: 0,
    }
  },
  methods: {
    calculatePosition() {
      //  position = (this.$refs.h3 as Element).getBoundingClientRect().right,
    },
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
    border-top: 3px solid $accent;
  }
  &.secondary {
    border-top: 3px solid $secondary;
  }
}

h2 {
  font-size: 36px;
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
