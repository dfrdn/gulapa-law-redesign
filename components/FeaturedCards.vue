<template>
  <div>
    <b-container>
      <b-row>
        <b-col>
          <section-title
            heading="Why Choose Us"
            class="d-lg-none"
          ></section-title>
        </b-col>
      </b-row>
      <b-row id="features" align-h="center">
        <b-col
          v-for="feature in features"
          :key="feature.heading"
          class="feature d-flex"
          cols="12"
          lg="4"
        >
          <b-row align-v="center" class="py-4">
            <b-col cols="4" class="text-center">
              <img
                class="img-fluid"
                :src="feature.icon"
                :alt="feature.heading"
              />
            </b-col>
            <b-col>
              <h2>{{ feature.heading }}</h2>
              <p>
                {{ feature.description }}
              </p>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      features: [
        {
          icon: require('~/assets/images/collaboration_icon.svg'),
          heading: 'Collaboration',
          description:
            'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo cum optio veroorem',
        },

        {
          icon: require('~/assets/images/legal-experts_icon.svg'),
          heading: 'Legal Experts',
          description:
            'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo cum optio veroorem',
        },
        {
          icon: require('~/assets/images/awards_icon.svg'),
          heading: 'Awards',
          description:
            'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Explicabo cum optio veroorem',
        },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
.feature {
  background: white;
  box-shadow: 0px 3px 6px 0px #0000000f;
  // flex: 0 1 400px;

  &:first-child {
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px;
  }

  &:last-child {
    border-top-right-radius: 10px;
    border-bottom-right-radius: 10px;
  }

  @media (max-width: 992px) {
    border-radius: 10px;
    margin: 10px 10px;
  }
}

@media (min-width: 992px) {
  #features {
    transform: translateY(-50%);
  }
}
</style>
