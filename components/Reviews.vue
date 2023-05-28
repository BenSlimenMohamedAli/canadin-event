<template>
  <section id="what-people-says">
    <div class="testimonial-heading-bg white-heading">
      <div class="container">
        <div class="row text-center">
          <div class="col-lg-12 col-md-12 col-sm-12">
            <span>{{ data.subtitle }}</span>
            <h2>{{ data.title }}</h2>
            <hr />
          </div>
        </div>
      </div>
    </div>
    <div id="what-client-says">
      <div class="container">
        <div class="row">
          <div class="col-lg-6 offset-lg-6 col-md-12 what-client-says-col">
            <div class="what-client-says-inn">
              <div class="owl-carousel owl-theme">
                <div
                  v-for="item in data.list"
                  :key="item.position"
                  class="item"
                >
                  <div class="user-info">
                    <figure>
                      <img src="images/testimonial_01.png" alt="user image" />
                      <figcaption>
                        <h4>
                          {{ item.name }}
                          <span>{{ item.position }}</span>
                        </h4>
                        <p>
                          {{ item.review }}
                        </p>
                      </figcaption>
                    </figure>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    data: {
      type: Object,
      default: null,
    },
  },
})
</script>
