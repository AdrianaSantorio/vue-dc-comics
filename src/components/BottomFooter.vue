<template>
  <div class="bottom-footer">
          <div class="container">
              <Button/>
              <section class="social">
                  <span>FOLLOW US</span>
                  <div>
                      <a v-for="(social,index) in socials" :key="index" :href="social.url" >
                          <img  :src="social.image" :alt="social.name">
                      </a>
                  </div>
              </section>
          </div>
      </div>
</template>

<script>
import Button from "./Button.vue";

export default {
    name: "bottom-footer",
    components: {
        Button,
    },
    data() {
        return {
            socials: [
                //immagini non funzionano, mi sa lezione dopo
                {name: "Facebook", url:"#", image:"../assets/img/footer-facebook.png"},
                {name: "Twitter", url:"#", image:"../assets/img/footer-twitter.png"},
                {name: "Youtube", url:"#", image:"../assets/img/footer-youtube.png"},
                {name: "Pinterest", url:"#", image:"../assets/img/footer-pinterest.png"},
                {name: "Periscope", url:"#", image:"../assets/img/footer-periscope.png"},
            ]
        }
    }

}
</script>

<style scoped lang="scss">
    @import "../assets/sass/_vars.scss";
    @import "../assets/sass/_mixins.scss";

    .bottom-footer {
        background-color: #303030;
        height: 120px;
        color: $main-color;
        font-size: 1.5rem;

    }

    .container {
        height: 100%;
        @include flex-between;  
    }

    .social {
        font-size: 800;
        @include flex-between;
    }
</style>