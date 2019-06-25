<template>
  <div class="layout">
    <navigation class="section-nav"></navigation>
    <div class="section-right">
      <home class="section-home"></home>
      <about class="section-about height-all">About</about>
      <exp class="section-exp height-all">exp</exp>
      <project class="section-project height-all">project</project>
      <skill class="section-skill height-all">skill</skill>
      <resume class="section-resume height-all">resume</resume>Ï
    </div>
  </div>
</template>
<script>
import navigation from "@/views/Navigation";
import home from "@/views/Home";
import about from "@/views/About";
import exp from "@/views/Experience";
import project from "@/views/Project";
import skill from "@/views/Skill";
import resume from "@/views/Resume";

export default {
  components: {
    navigation,
    home,
    about,
    exp,
    project,
    skill,
    resume
  }
};
</script>
<style lang="scss">
</style>

