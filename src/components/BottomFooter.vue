<template>
  <div class="bottom-footer">
          <div class="container">
              <SignUpButton />
              <section class="social">
                  <span>FOLLOW US</span>
                  <div>
                      <a v-for="(social,index) in socials" :key="index" :href="social.url" >
                          <img  :src="require(`../assets/img/${social.image}`)" :alt="social.name">
                      </a>
                  </div>
              </section>
          </div>
      </div>
</template>

<script>
import SignUpButton from "./SignUpButton.vue";

export default {
    name: "bottom-footer",
    components: {
        SignUpButton,
    },
    data() {
        return {
            socials: [
                //immagini non funzionano, mi sa lezione dopo
                {name: "Facebook", url:"#", image:"footer-facebook.png"},
                {name: "Twitter", url:"#", image:"footer-twitter.png"},
                {name: "Youtube", url:"#", image:"footer-youtube.png"},
                {name: "Pinterest", url:"#", image:"footer-pinterest.png"},
                {name: "Periscope", url:"#", image:"footer-periscope.png"},
            ]
        }
    },
    methods: {
        // getImage(index) {
        //     return require(this.socials[index].image);
        // }
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
        span {
            margin: 15px;
        }
        img {
            margin: 5px;
        }
    }
</style>