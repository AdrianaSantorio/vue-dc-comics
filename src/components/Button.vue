<template>
  <div>
      <a href="#">SIGN UP NOW</a>
  </div>
</template>

<script>
export default {
    name: "Button",
}
</script>

<style scoped lang="scss">

@import "../assets/sass/_vars.scss";

a {
    border: 3px solid $main-color;
    padding: 0.9rem;
    color: white;
    font-size: 1.1rem;
}

</style>