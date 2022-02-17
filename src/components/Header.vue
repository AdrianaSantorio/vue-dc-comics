<template>
  <header>
    <div class="container h-100">
        <!-- logo -->
        <figure>
            <img src="../assets/img/dc-logo.png" alt="logo DC">
        </figure>
        <!-- navbar -->
        <nav class="h-100">
            <ul class="h-100">
                <li v-for="(link, index) in links" :key="index" class="h-100" :class="{active: link.active}" @mouseover="isActive(true,index)"  @mouseleave="isActive(false,index)">
                    <a :href="link.url">{{link.text}}</a>
                </li>
            </ul>
        </nav>
    </div>
  </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            links: [
                {text: "CHARACTERS", url: "#", active: false},
                {text: "COMICS", url: "#", active: false},
                {text: "MOVIES", url: "#", active: false},
                {text: "TV", url: "#", active: false},
                {text: "GAMES", url: "#", active: false},
                {text: "COLLECTIBLES", url: "#", active: false},
                {text: "VIDEOS", url: "#", active: false},
                {text: "FANS", url: "#", active: false},
                {text: "NEWS", url: "#", active: false},
                {text: "SHOP", url: "#", active: false},
            ]
        }
    },
    methods: {
        isActive(status, index) {
            this.links[index].active = status;
            //perchè non funziona mouseleave?
        }
    }
}
</script>

<style scoped lang="scss">

    @import "../assets/sass/_mixins.scss";
    @import "../assets/sass/_vars.scss";

    header {

        height: 120px;
        background-color: white;
        img {
            height: 90px;
        }
    }

    
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;     
    }

    nav ul {
        display: flex;
        align-items: center;

        li {
            display: flex;
            align-items: center;
            list-style-type: none;
            margin: 5px;
            border-bottom: 6px solid transparent;

            a{
            font-weight: 700;
            font-size: 0.8rem;
            }

            &.active {
                color: #0282F9;
                border-bottom: 6px solid $main-color;
            }
        }
    }
</style>