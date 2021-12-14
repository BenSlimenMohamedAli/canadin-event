<template>
  <section id="counts-sec">
    <div class="container">
      <div class="row">
        <div
          v-for="item in data.counts"
          :key="item.title"
          class="col-lg-3 col-md-3 col-sm-3 count-box"
        >
          <div class="milestone-counter">
            <i class="fa" :class="item.icon"></i>
            <h2 class="stat-count highlight">{{ item.value }}</h2>
            <span>{{ item.title }}</span>
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
