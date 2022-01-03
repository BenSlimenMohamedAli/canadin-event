<template>
  <section id="annual-conference-sec">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 col-md-6 col-sm-12">
          <figure class="video-bg-sec">
            <img src="images/video-bg.jpg" alt="video-bg" />
            <figcaption>
              <button
                class="btn btn-primary"
                data-toggle="modal"
                data-target="#exampleModalLong"
              >
                <img src="images/video.png" alt="video" />
                <p>{{ data.watchVideo }}</p>
              </button>
            </figcaption>
          </figure>
        </div>
        <div class="col-lg-6 col-md-6 col-sm-12">
          <div class="video-info pt-3">
            <h3>{{ data.title }}</h3>
            <hr />
            <p style="font-size: 20px !important" v-html="data.content"></p>
            <ul class="view-btns">
              <li>
                <a
                  href="https://docs.google.com/forms/d/e/1FAIpQLScQjWkFm0PpNP7WVNasNyUhuW5eHYM2OlrMEcJCU_vOa0x1QA/viewform?usp=pp_url&entry.1994969570=Option+n%C2%B0+1 "
                  class="view button--antiman button--inverted-alt mt-2"
                  target="_blank"
                  >{{ data.button1 }}</a
                >
              </li>
              <li>
                <a
                  href="/Programme Master Class.pdf"
                  target="_blank"
                  class="view button--antiman button--inverted-alt mt-2"
                  >{{ data.button2 }}</a
                >
              </li>
            </ul>
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
