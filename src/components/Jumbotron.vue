<template>
  <div class="jumbotron">
      <img :src="jumbotronImage" alt="DC comics">
  </div>
</template>

<script>



export default {
    name: "Jumbotron",
    props: [
        "jumbotronImage"
    ]
}
</script>

<style scoped lang="scss">
    .jumbotron {
        max-height: 300px;
        overflow: hidden;
    }

</style>