<template>
  <section id="main-banner-sec">
    <div class="container">
      <div class="row">
        <div class="col-lg-7 col-md-12 col-sm-12">
          <div class="banner-left-bar">
            <ul class="time-location">
              <li>
                <i class="fa fa-calendar-o"></i>
                {{ data.eventDate }}
              </li>

              <li><i class="fa fa-map-marker"></i> {{ data.eventPlace }}</li>
            </ul>
            <h1>{{ data.title }}</h1>
            <hr />
            <p class="text-white">{{ data.description }}</p>
            <div id="defaultCountdown" class="mt-5"></div>
            <ul class="social-icons mb-5">
              <li>
                <a :href="data.facebookLink" target="_blank"
                  ><i class="fa fa-facebook"></i
                ></a>
              </li>
              <li>
                <a :href="data.linkedinLink" target="_blank"
                  ><i class="fa fa-linkedin"></i
                ></a>
              </li>
              <li>
                <a :href="data.youtubeLink" target="_blank"
                  ><i class="fa fa-youtube"></i
                ></a>
              </li>
              <li>
                <a :href="data.instagramLink" target="_blank"
                  ><i class="fa fa-instagram"></i
                ></a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-lg-5 col-md-12 col-sm-12">
          <div class="register-form" style="height: 100%">
            <form
              id="contact"
              method="post"
              class="userform"
              action="thank-you.html"
              onsubmit="return validateForm()"
            >
              <br />
              <div>
                <h5
                  class="text-white h4"
                  v-html="data.rightBox.description"
                ></h5>
                <p class="text-white mt-5">
                  *(Offre valable sous condition d’engagement pour signature de
                  5 contrats de travail)
                </p>
              </div>
              <br />
              <div id="contact_submit" class="input-box mr mt-5">
                <a
                  href="https://docs.google.com/forms/d/e/1FAIpQLScQjWkFm0PpNP7WVNasNyUhuW5eHYM2OlrMEcJCU_vOa0x1QA/viewform?usp=pp_url&entry.1994969570=Option+n%C2%B0+1 "
                  class="send_btn submit-btn btn"
                  target="_blank"
                  type="submit"
                >
                  {{ data.rightBox.button }}
                </a>
              </div>
              <strong>(Dernier délai d’inscription: 10 juin 2023) </strong>
            </form>
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
