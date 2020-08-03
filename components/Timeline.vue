<template>
  <div>
    <ol>
      <li v-for="event in timelineEvents" :key="event.event">
        <div class="dot m-2"></div>
        <div class="entry d-flex">
          <div class="year my-1">{{ event.year }}</div>
          <div class="event">{{ event.event }}</div>
        </div>
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
  @media (max-width: 992px) {
    flex-direction: column;
    justify-content: baseline;
    align-items: center;
  }
  // background: black;

  &::before {
    content: '';
    position: absolute;
    width: 80%;
    height: 3px;
    background-color: white;
    margin: 0 auto;
    top: 50%;
    transform: translateY(calc(50% + 3px));

    @media (max-width: 992px) {
      content: '';
      position: absolute;
      width: 3px;
      height: 100%;
      background-color: white;
      margin: 0 auto;
      top: 0;
      transform: translateY(50px);
    }
  }

  li {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;

    &:first-child {
      .entry {
        align-items: center;
      }
      .year {
        width: 58px;
        line-height: 58px;
        background-color: white;
        border-radius: 50%;
        border: 1px solid #fff;

        @media (max-width: 992px) {
          order: 1;
        }
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

      @media (max-width: 992px) {
        flex-flow: row wrap;
        text-align: left;
        transform: translateX(calc(50% - 15px));
      }
    }

    .entry {
      flex-direction: column;
    }

    @media (max-width: 992px) {
      align-items: flex-start;
    }

    &:nth-of-type(even) {
      flex-direction: column-reverse;

      @media (max-width: 992px) {
        flex-flow: row-reverse wrap;
        text-align: right;
        transform: translateX(calc(-50% + 15px));
      }

      .entry {
        flex-direction: column-reverse;
        @media (max-width: 992px) {
          flex-direction: column;
        }
      }
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
