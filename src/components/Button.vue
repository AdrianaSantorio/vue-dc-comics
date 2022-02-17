<template>
      <button>{{buttonText}}</button>
</template>

<script>
export default {
    name:"Button",
    props:["buttonText"]

}
</script>

<style scoped lang="scss">
  @import "../assets/sass/_vars.scss";

  button {
    display: inline-block;
    background-color: $main-color;
    color: $main-text-color;
    padding: 0.5rem;
    min-width: 180px;
    border: none;
    cursor: pointer;
    text-align: center;
    margin: 15px 0;

  }
</style>