<template>
  <section id="event-schedule-sec">
    <div class="container">
      <div class="row text-center sec-black-hadding">
        <div class="col-lg-12 col-md-12 col-sm-12">
          <h2>{{ data.title }}</h2>
          <hr />
        </div>
      </div>
      <div id="exTab1">
        <ul class="nav nav-pills" style="justify-content: center">
          <li
            v-for="(item, index) in data.list"
            :key="index"
            :class="{ active: index === 0 }"
          >
            <button>
              <a style="padding-right:30px !important; padding-left:30px !important" :href="'#' + index + 'a'" data-toggle="tab">
                {{ item.topTitle }}
                <span>{{ item.date }}</span>
              </a>
            </button>
          </li>
        </ul>

        <div class="tab-content clearfix">
          <div
            v-for="(item, index) in data.list"
            :id="index + 'a'"
            :key="index"
            :class="{ active: index === 0 }"
            class="tab-pane"
          >
            <h4 class="text-center my-3">{{ item.title }}</h4>
            <div class="tab-content">
              <div class="tab-pane active">
                <div v-if="index == 0" class="schedule">
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers1" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
                  </div>
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers2" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
                  </div>
                </div>
                <div v-if="index == 1" class="schedule justify-content-center">
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers3" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
                  </div>
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers4" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
                  </div>
                </div>
                <div v-if="index == 2" class="schedule justify-content-center">
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers5" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
                  </div>
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers6" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
                  </div>
                </div>
                <div v-if="index == 3" class="schedule justify-content-center">
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers7" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
                  </div>
                  <div class="schedule-content col-md-12 col-lg-6">
                    <div v-for="speaker in data.speakers8" :key="speaker.title">
                      <Speaker :speaker="speaker" :index="index" />
                    </div>
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
      default: null
    }
  }
})
</script>
