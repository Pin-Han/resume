<template>
  <div class="layout">
    <navigation class="section-nav"></navigation>
    <div class="section-right">
      <home class="section-home"></home>
      <about></about>
    </div>
  </div>
</template>
<script>
import navigation from "@/views/Navigation";
import home from "@/views/Home";
import about from "@/views/About";

export default {
  components: {
    navigation,
    home,
    about
  }
};
</script>
<style lang="scss">
</style>

