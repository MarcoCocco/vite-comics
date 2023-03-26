<script>
import AppNavbar from "./components/AppNavbar.vue"
import AppJumbotron from "./components/AppJumbotron.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"

export default {
  data() {
    return {

    }
  },

  components: {
    AppNavbar,
    AppJumbotron,
    AppMain,
    AppFooter
  }

}
</script>

<template>

  <AppNavbar></AppNavbar>

  <AppJumbotron></AppJumbotron>

  <AppMain></AppMain>

  <AppFooter></AppFooter>

</template>

<style lang='scss'>

.container-centered {
  max-width: 1200px;
  margin: 0 auto;
}

</style>
