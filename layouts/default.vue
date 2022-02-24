<template>
  <div>
    <Header />
    <IndexPage/>
    <Footer />
  </div>
</template>

<script>
import Header from "../components/Header";
import Footer from "../components/Footer";
import IndexPage from "../pages/index";
export default {
  name: "default",
  components: {
    Header,
    Footer,
    IndexPage,
  },
};
</script>

<style>
</style>