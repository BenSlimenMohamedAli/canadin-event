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
            <h3 style="font-size: 25px">{{ data.title }}</h3>
            <hr />
            <p style="font-size: 12px !important" v-html="data.content"></p>

            <ul class="view-btns">
              <li>
                <a
                  href="https://docs.google.com/forms/d/e/1FAIpQLSdK0sTeYCYHLjfBrOS-VqESAtBoKhEsnK5Sfpt7okAr9Dv8mw/viewform"
                  class="view button--antiman button--inverted-alt mt-2"
                  target="_blank"
                  >{{ data.button1 }}</a
                >
              </li>
              <li>
                <a
                  href="https://drive.google.com/file/d/186pGyTSTdKxh-WifSqI3xueZfeW_Yh7V/view"
                  class="view button--antiman button--inverted-alt mt-2"
                  target="_blank"
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
      default: null,
    },
  },
})
</script>
