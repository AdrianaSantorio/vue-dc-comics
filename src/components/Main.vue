<template>
  <main>
      <Jumbotron :jumbotron-image="getImageUrl(JumbotronUrl)"/>
      <div class="current-series-gallery">
        <div class="container">
          <ul>
            <li :v-for="(serie, index) in currentSeries" :key="index" >
              <Card :serie="serie"/>
              ciao
            </li>
          </ul>
        </div>
      </div>
  </main>
</template>

<script>

import Jumbotron from "./Jumbotron.vue"
import Card from "./Card.vue"

export default {
    name: "main",
    props: ["currentSeries"],
    components: {
      Jumbotron, Card,
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