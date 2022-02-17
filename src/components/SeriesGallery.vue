<template>
  <div class="series-gallery container">
        <Label :label="label"/>
        <ul>
            <li v-for="(serie, index) in series" :key="index" >
                <a href="#">
                <Card :serie="serie"/>
                </a>            
            </li>
        </ul>
        <Button button-text="LOAD MORE"/>
    </div>
</template>

<script>
import Card from "./Card.vue"
import Label from "./Label.vue"
import Button from "./Button.vue"

export default {
    name: "SeriesGallery",
    components: { 
    Card,Label,Button,
    },
    props: ["series","label"]
}
</script>

<style scoped lang="scss">
@import "../assets/sass/_vars.scss";

.series-gallery {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 15px 0;
    position: relative;
}

ul {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    li {
        flex-basis: calc(100% / 12 * 2);
        max-width: calc(100% / 12 * 2);
        color: $main-text-color;
        padding: 10px;
    }
}

</style>