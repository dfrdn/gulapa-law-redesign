<template>
  <div>
    <b-list-group>
      <b-list-group-item
        v-for="lawyer in lawyers"
        :key="lawyer.slug"
        :to="`/lawyers/${lawyer.slug}`"
        :class="{ active: active === lawyer.name }"
        >{{ lawyer.name }}</b-list-group-item
      >
    </b-list-group>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    active: {
      type: String,
      required: true,
    },
    lawyers: {
      type: Array,
      required: true,
    },
  },
})
</script>

<style scoped></style>
