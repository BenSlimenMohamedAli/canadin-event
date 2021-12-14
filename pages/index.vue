<template>
  <section>
    <!-- Main Header -->
    <TopHeader />
    <!-- /End Main Header -->
    <!-- Main content here -->
    <main class="">
      <!-- Banner & From -->
      <MainBanner :data="mainBanner" />
      <!-- / End Banner & From -->
      <!-- Welcome to Annual Conference -->

      <!-- / End Welcome to Annual Conference -->
      <AnnualConference :data="annualConference" />
      <!-- Counts -->
      <Counts :data="counts" />
      <!-- /End Counts -->
      <!-- Speakers -->
      <ToolsBox :data="toolsBox" />
      <!-- /End Speakers -->
      <!-- Why Choose Us -->
      <WhyChooseUs :data="whyChooseUs" />
      <!-- Why Choose Us End -->
      <!-- Event Schedule Section-->
      <Schedule :data="schedule" />
      <!-- Event Schedule End-->
      <div class="clearfix"></div>

      <!-- Previous Events sec -->

      <Gallery />
      <!-- /End Previous Events sec -->

      <!-- Upcoming Events & News sec -->
      <UpcomingEvents :data="upcomingEvents" />
      <!-- /End Upcoming Events & News sec -->

      <!-- /Main content End -->

      <!-- /Subscribe newslatter -->
      <Newsletter />
      <!-- END Subscribe newslatter -->

      <Contact />

      <Footer />
    </main>

    <!-- Annual Conference Video -->

    <AnnualModel />
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  async asyncData({ $content }) {
    const mainBanner = await $content('main-banner').fetch()
    const annualConference = await $content('annual-conference').fetch()
    const counts = await $content('counts').fetch()
    const toolsBox = await $content('tools-box').fetch()
    const whyChooseUs = await $content('why-choose-us').fetch()
    const schedule = await $content('schedule').fetch()
    const upcomingEvents = await $content('upcoming-events').fetch()

    return {
      mainBanner,
      annualConference,
      counts,
      toolsBox,
      whyChooseUs,
      schedule,
      upcomingEvents
    }
  },
  data() {
    return {
      slideIndex: 1
    }
  },
  mounted() {
    this.showSlides(this.slideIndex)
  },
  methods: {
    showSlides(n: number) {
      let i
      const slides = document.getElementsByClassName('mySlides') as any
      const dots = document.getElementsByClassName('demo')
      if (n > slides.length) {
        this.slideIndex = 1
      }
      if (n < 1) {
        this.slideIndex = slides.length
      }
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = 'none'
      }
      for (i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(' active', '')
      }
      slides[this.slideIndex - 1].style.display = 'block'
    }
  }
})
</script>
