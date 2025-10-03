<script setup>
import Collabs from './components/Collabs.vue';
import Header from './components/Header.vue'
import Hero from './components/Hero.vue';
import Support from './components/Support.vue';
import Benifit from './components/Benifit.vue';
import ChoosePlan from './components/ChoosePlan.vue';
import GetStarted from './components/GetStarted.vue';
import Footer from './components/Footer.vue';
import OurFeature from './components/OurFeature.vue';

</script>

<template>
  <div class="relative overflow-hidden">
    <div class="relative z-10">
      <Header />
      <Hero />
      <Collabs />
      <Support />
      <OurFeature />
      <Benifit />
      <ChoosePlan />
      <GetStarted />
      <Footer />
    </div>
    <div class="bg-dark-red size-[634px] rounded-[9999px] blur-[500px] absolute -top-[280px] -left-[317px]"></div>
    <div class="bg-light-pink size-[634px] rounded-[9999px] blur-[500px] absolute -top-[364px] -right-[225px]"></div>
    <div class="bg-light-red size-[634px] rounded-[9999px] blur-[500px] absolute -top-[270px] -right-[317px]"></div>

  </div>
</template>

<style scoped></style>
