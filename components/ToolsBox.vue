<template>
  <section id="our-speakers-sec">
    <div class="container">
      <div class="row">
        <div class="col-lg-4 col-md-6 col-sm-6">
          <div class="event-speakers">
            <span>{{ data.subtitle }}</span>
            <h3>{{ data.title }}</h3>
            <hr />
            <div class="info_height">
              <p v-html="data.description"></p>
            </div>
          </div>
        </div>
        <div
          v-for="item in data.tools"
          :key="item.title"
          class="col-lg-4 col-md-6 col-sm-6"
        >
          <figure class="speaker-box">
            <img :src="item.image" :alt="item.title" />
            <figcaption style="right: 0; left: 0">
              <h4>{{ item.title }}</h4>
              <p><br /><br /><br /><br /><br /></p>
            </figcaption>
          </figure>
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
