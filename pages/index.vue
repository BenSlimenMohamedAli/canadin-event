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

      <Reviews :data="reviews" />

      <Services :data="services" />

      <Sponsors />

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

      <Location />

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
    const reviews = await $content('reviews').fetch()
    const services = await $content('services').fetch()

    return {
      mainBanner,
      annualConference,
      counts,
      toolsBox,
      whyChooseUs,
      schedule,
      upcomingEvents,
      reviews,
      services,
    }
  },
})
</script>
