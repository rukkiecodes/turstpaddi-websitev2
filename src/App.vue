<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
export default {
  data() {
    return {};
  },
  methods: {
    backToTop() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    },
  },
  components: { Header, Footer },
};
</script>

<template>
  <div class="app">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Montserrat&display=swap");
.app {
  font-family: "Montserrat";
  overflow-x: hidden;
}
</style>
