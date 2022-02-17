<template>
    <div class="Card">
        <figure>
            <img :src="serie.thumb" alt="">
            <figcaption>ciao</figcaption>
        </figure>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ["serie"],
}
</script>

<style>

</style>