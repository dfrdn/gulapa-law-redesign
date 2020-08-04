<template>
  <nuxt-link to="/contact">
    <div id="consult">
      <i class="fas fa-comment"></i>
    </div>
  </nuxt-link>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
#consult {
  border-radius: 50%;
  background: $primary;
  width: 50px;
  line-height: 50px;
  position: fixed;
  right: 25px;
  bottom: 25px;
  z-index: 4000;
  text-align: center;
  box-shadow: 2px 2px 6px 0 #0000007f;
  font-size: 20px;
}

a {
  color: white;
}
</style>
