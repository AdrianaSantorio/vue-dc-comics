<template>
  <main>
      <Jumbotron :jumbotron-image="getImageUrl(JumbotronUrl)"/>
      <!-- Current Series -->
      <SeriesGallery :series="currentSeries" label="CURRENT SERIES" />
      <Featured />
  </main>
</template>

<script>

import Jumbotron from "./Jumbotron.vue"
import SeriesGallery from "./SeriesGallery.vue"
import Featured from "./Featured.vue"



export default {
    name: "main",
    props: ["currentSeries"],
    components: {
      Jumbotron, SeriesGallery, Featured,
    },
    data() {
      return {
        JumbotronUrl: "jumbotron.jpg",

      }
    },
    methods: {
      getImageUrl(imageUrl) {
        return require("../assets/img/" + imageUrl)
      } 

    }
}
</script>

<style scoped lang="scss">

</style>