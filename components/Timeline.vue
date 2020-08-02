<template>
  <div>
    <ol>
      <li v-for="event in timelineEvents" :key="event.event"></li>
    </ol>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      timelineEvents: [
        { year: '2015', event: 'Gulapa Law was eastablished' },
        { year: '2016', event: 'Botique Law Firm of the Year' },
        { year: '2017', event: 'Established New York Office' },
        {
          year: '2018',
          event: 'Established San Francisco Representative Office',
        },
        { year: '2019', event: 'Established Cebu Office' },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
.year {
  color: $accent;
}

.event {
  color: white;
}
</style>
