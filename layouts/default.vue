<template>
  <div>
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Header from "../components/Header";
import Footer from "../components/Footer";
export default {
  name: "default",
  components: {
    Header,
    Footer,
  },
};
</script>

<style>
</style>