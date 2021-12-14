<template>
  <section id="upcoming-event-sec">
    <div class="container">
      <div class="row text-center sec-black-hadding">
        <div class="col-lg-12 col-md-12 col-sm-12">
          <h2>Nos evennements</h2>
          <hr />
        </div>
      </div>
      <div class="row">
        <div class="col-lg-12 col-md-12">
          <div id="upcoming-events-slider" class="news-slider">
            <div class="owl-carousel owl-theme">
              <div v-for="item in data.list" :key="item" class="item">
                <div class="news-block">
                  <figure>
                    <iframe
                      id="ytplayer"
                      style="width: 100%"
                      class="embed-responsive-item"
                      :src="item.link"
                      frameborder="0"
                      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                      allowfullscreen
                    ></iframe>
                    <figcaption>
                      <div class="date">{{ item.date }}</div>
                      <h3>
                        <a href="#">{{ item.title }}</a>
                      </h3>
                    </figcaption>
                  </figure>
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
      default: null
    }
  }
})
</script>
