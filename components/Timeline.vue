<template>
  <div>
    <ol>
      <li
        v-for="event in timelineEvents"
        :key="event.event"
        class="text-center"
      >
        <div class="dot my-2"></div>
        <div class="year my-1">{{ event.year }}</div>
        <div class="event">{{ event.event }}</div>
      </li>
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
ol {
  list-style-type: none;
  display: flex;
  align-items: baseline;
  // background: black;

  &::before {
    content: '';
    position: absolute;
    width: 80%;
    height: 3px;
    background-color: white;
    margin: 0 auto;
    top: 50%;
    transform: translateY(50%);
  }

  li {
    display: flex;
    flex-direction: column;
    align-items: center;

    &:first-child {
      .year {
        width: 58px;
        line-height: 58px;
        background-color: white;
        border-radius: 50%;
        border: 1px solid #fff;
      }
      transform: translateY(-30px);
      // align-self: start;
    }

    &:not(:first-child) {
      .dot {
        width: 15px;
        height: 15px;
        border-radius: 50%;
        background-color: white;
        border: 1px solid #fff;
      }

      transform: translateY(20px);
    }

    &:nth-of-type(even) {
      flex-direction: column-reverse;
    }

    .year {
      color: $accent;
    }

    .event {
      color: white;
      max-width: 18ch;
    }
  }
}
</style>
