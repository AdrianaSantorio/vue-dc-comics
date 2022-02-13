<template>
  <footer>
      <UpperFooter />
      <BottomFooter />
  </footer>
</template>

<script>
import UpperFooter from "./UpperFooter.vue";
import BottomFooter from "./BottomFooter.vue";

export default {
    name: "Footer",
    components: {
        UpperFooter,
        BottomFooter,
    }
    
}
</script>

<style scoped lang="scss">

</style>