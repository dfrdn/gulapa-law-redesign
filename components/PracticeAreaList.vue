<template>
  <div>
    <b-list-group>
      <b-list-group-item
        v-for="practiceArea in allPracticeAreas"
        :key="practiceArea.slug"
        :to="`/practice-areas/${practiceArea.slug}`"
        :class="{ active: active === practiceArea.title }"
      >{{ practiceArea.title }}</b-list-group-item>
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
    allPracticeAreas: {
      type: Array,
      required: true,
    },
  },
})
</script>

<style scoped></style>
