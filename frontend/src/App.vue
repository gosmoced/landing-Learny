<script setup>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Features from "./components/Features.vue";
import Steps3 from "./components/Steps3.vue";
import Companion from "./components/Companion.vue";
import Experience from "./components/Experience.vue";
import Designed from "./components/Designed.vue";
import Price from "./components/Price.vue"
import Ready from "./components/Ready.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <div class="wrapper">
    <Header />
    <main class="content">
      <Hero />
      <Features />
      <Steps3 />
      <Companion />
      <Experience />
      <Designed />
      <Price />
      <Ready />
    </main>
    <Footer />
  </div>
</template>

<style scoped>
.content{
  max-width: 1280px;
  width: 95%;
  margin: 0 auto;
  padding: 0 10px;
}
@media(max-width: 768px){
  .content{
    width: 95%;
    margin: 0 auto;
  }
}
</style>
