<template>
  <div id="app">
    <Head></Head>
    <CentalTest></CentalTest>
  </div>
</template>

<script>
  import Head from "./components/Head";
  import CentalTest from "./components/CentalTest";

export default {
  name: 'app',
  components: {Head,CentalTest},
  data() {
    return {
    };
  },
  methods: {
  },

}
</script>

<style>
  @import "assets/less/fy.css";

  /*@import "https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css";*/
</style>
