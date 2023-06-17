<template>
  <section>
    <div class="event-schedule position-relative">
      <figure>
        <img :src="speaker.image" alt="speaker-image" />
        <!-- <figcaption>
          <ul class="event-icon">
            <li>
              <a target="_blank" :href="speaker.linkedin"
                ><i class="fa fa-linkedin"></i
              ></a>
            </li>
          </ul>
        </figcaption> -->
      </figure>
      <div class="event-info">
        <p>
          <i class="fa fa-clock-o" aria-hidden="true"></i>{{ speaker.name }}
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
      default: null,
    },
    index: {
      type: Number,
      default: null,
    },
  },
})
</script>
