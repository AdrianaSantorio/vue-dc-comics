<template>
  <div class="featured">
        <div class="container h-100">
            <ul class="h-100">
                <li v-for="(feature, index) in features" :key="index" class="h-100">
                    <a href="#"><img :src="getImageUrl(feature.url)" :alt="feature.text"></a>
                    <a href="#">{{feature.text}}</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: "Featured",
    data() {
        return {
            features: [
                {
                    url:"buy-comics-digital-comics.png",
                    text:"DIGITAL COMICS",
                },
                {
                    url:"buy-comics-merchandise.png",
                    text:"DC MERCHANDISE",
                },
                {
                    url:"buy-comics-subscriptions.png",
                    text:"SUBSCRIPTION",
                },
                {
                    url:"buy-comics-shop-locator.png",
                    text:"COMIC SHOP LOCATOR",
                },
                {
                    url:"buy-dc-power-visa.svg",
                    text:"DC POWER VISA",
                },
            ]
        }
    },
    methods: {
        getImageUrl(imageUrl) {
        return require(`../assets/img/${imageUrl}`)
      } 
    }
}
</script>

<style scoped lang="scss">

@import "../assets/sass/_vars.scss";

.featured {
    background-color: $main-color;
    color: $main-text-color;
    height: 120px;
    padding: 30px 15px;

    ul {
        display: flex;
        align-items: center;
        justify-content: space-between;
        li {
            display: flex;
            align-items: center;

            a {
                margin: 0 15px;
            }
        }
    }

    img {
        height: 50px;
        width: auto;
    }
}

</style>