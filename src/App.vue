<template>
  <div id="app">
    <Hero />
    <Items />
    <Radiacion />
    <InfoOne />
    <PageOne />
    <InfoTwo />
    <PageTwo />
    <InfoThree />
    <PageThree />
    <Blog />
    <FAQ />
    <Footer />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Items from "./components/Items.vue";
import Radiacion from "./components/Radiacion.vue";

import InfoOne from "./components/InfoOne.vue";
import PageOne from "./components/PageOne.vue";
import InfoTwo from "./components/InfoTwo.vue";
import PageTwo from "./components/PageTwo.vue";
import InfoThree from "./components/InfoThree.vue";
import PageThree from "./components/PageThree.vue";

import Slider from "./components/Slider.vue";
import Blog from "./components/Blog.vue";
import FAQ from "./components/FAQ.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Hero,
    Items,
    Radiacion,
    InfoOne,
    PageOne,
    InfoTwo, 
    PageTwo,
    InfoThree,
    PageThree,
    /* Slider, */
    Blog,
    FAQ,
    Footer,
  },
};
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
  background-color: #E5E5E5;
  user-select: none;
  /* width: 100vw; */
  overflow-x: hidden;
}
</style>
