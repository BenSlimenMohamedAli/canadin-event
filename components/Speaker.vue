<template>
  <section>
    <div class="event-schedule position-relative">
      <div v-if="speaker.visibleIndex !== index" class="mask"></div>
      <figure>
        <img :src="speaker.image" alt="speaker-image" />
        <figcaption>
          <ul class="event-icon">
            <li>
              <a target="_blank" :href="speaker.linkedin"
                ><i class="fa fa-share-alt"></i
              ></a>
            </li>
          </ul>
        </figcaption>
      </figure>
      <div class="event-time">
        <h4>
          <i class="fa fa-clock-o" aria-hidden="true"></i>{{ speaker.time }}
        </h4>
      </div>
      <div class="event-info">
        <p>
          <i class="fa fa-microphone" aria-hidden="true"></i>{{ speaker.name }}
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    speaker: {
      type: Object,
      default: null
    },
    index: {
      type: Number,
      default: null
    }
  }
})
</script>

<style scoped>
.mask {
  position: absolute;
  top: 0;
  right: O;
  left: 0;
  bottom: 0;
  background: gray;
  width: 100%;
  z-index: 1111111;
}
</style>
