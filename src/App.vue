<template>
  <div id="app">
    <Hero />
    <Blog />
    <FAQ />
    <Footer />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Blog from "./components/Blog.vue";
import FAQ from "./components/FAQ.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Hero,
    Blog,
    FAQ,
    Footer,
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #E5E5E5;
  user-select: none;
}
</style>
