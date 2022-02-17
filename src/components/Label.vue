<template>
  <div class="label">
        <span>{{label}}</span>
    </div>
</template>

<script>
export default {
    name: "Label",
    props: ["label"],
}
</script>

<style scoped lang="scss">

@import "../assets/sass/_vars.scss";


.label {
    position: absolute;
    top: 0;
    left: 0;
    display: inline-block;
    min-width: 220px;
    padding: 0.5rem;
    text-align: center;
    font-weight: bold;
    font-size: 1.1rem;
    color: $main-text-color;
    background-color: $main-color;
    transform: translate(0, -50%);
}


</style>