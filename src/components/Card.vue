<template>
    <div class="Card">
        <figure>
            <img :src="serie.thumb" :alt="serie.series">
            <figcaption>{{serie.series.toUpperCase()}}</figcaption>
        </figure>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ["serie"],
}
</script>

<style scoped lang="scss">
    figure {
        width: 100%;

        img {
        width: 100%;
        height: auto;
        }
    }
    
    
</style>