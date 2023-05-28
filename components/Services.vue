<template>
  <section id="event-packages-sec">
    <div class="container">
      <div class="row text-center sec-black-hadding">
        <div class="col-lg-12 col-md-12 col-sm-12">
          <span>{{ data.subtitle }}</span>
          <h2>{{ data.title }}</h2>
          <hr />
        </div>
      </div>
      <div class="row eventpackage">
        <div
          v-for="item in data.list"
          :key="item.title"
          class="col-lg-3 col-sm-6 col-md-6 event-priceing"
        >
          <div class="inner-pricing">
            <div class="plan-name">
              <h6>{{ item.title }}</h6>
            </div>
            <div class="plan-details">
              <ul>
                <li v-for="subitem in item.list" :key="subitem.title">
                  <i class="fa fa-check" aria-hidden="true"></i>
                  {{ subitem.title }}
                </li>
              </ul>
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
