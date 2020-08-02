<template>
  <div>
    <h3 ref="h3">Who We Are {{ position }}</h3>
    <hr />
    <h2>Blabla</h2>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
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

<style scoped></style>
