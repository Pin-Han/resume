<template>
  <div class="layout">
    <div class="section-nav">
      <div class="all-nav">
        <div class="nav">
          <div class="nav__title" id="home">
            <img src="@/assets/image/self.jpeg" alt="self" class="nav__title--img">
            <p class="nav__title--name">林品翰</p>
          </div>
          <ul class="nav__router">
            <li class="nav__item" id="about">
              <i class="fas fa-user nav__item--icon"></i>
              <a href="#" class="nav__item--direct">About</a>
            </li>
            <li class="nav__item" id="exp">
              <i class="fas fa-lightbulb nav__item--icon"></i>
              <a href="#" class="nav__item--direct">Experience</a>
            </li>
            <li class="nav__item" id="project">
              <i class="fas fa-briefcase nav__item--icon"></i>
              <a href="#" class="nav__item--direct">Project</a>
            </li>
            <li class="nav__item" id="skill">
              <i class="far fa-chart-bar nav__item--icon"></i>
              <a href="#" class="nav__item--direct">Skill</a>
            </li>
            <li class="nav__item" id="resume">
              <i class="fas fa-file nav__item--icon"></i>
              <a href="#" class="nav__item--direct">Resume</a>
            </li>
            <li class="nav__item" id="contact">
              <i class="fas fa-phone nav__item--icon"></i>
              <a href="#" class="nav__item--direct">Contact</a>
            </li>
          </ul>
        </div>
        <div class="copyright">
          Copyright
          <i class="far fa-copyright"></i> 2019 Pin-Han Lin All Rights Reserved
        </div>
      </div>
    </div>
    <div class="section-right" id="right">

      <home class="section-home" id="nav-0"></home>
      <about class="section-about height-all" id="nav-1"></about>
      <exp class="section-exp height-all" id="nav-2">exp</exp>
      <project class="section-project height-all" id="nav-3">project</project>
      <skill class="section-skill height-all" id="nav-4">skill</skill>
      <resume class="section-resume height-all" id="nav-5">resume</resume>
      <contact class="section-resume height-all" id="nav-6">contact</contact>
    </div>
  </div>
</template>
<script>
import $ from "jquery";
import navigation from "@/views/Navigation";
import home from "@/views/Home";
import about from "@/views/About";
import exp from "@/views/Experience";
import project from "@/views/Project";
import skill from "@/views/Skill";
import resume from "@/views/Resume";
import contact from "@/views/Contact";

export default {
  components: {
    navigation,
    home,
    about,
    exp,
    project,
    skill,
    resume,
    contact
  },
  data() {
    return {
      scrolling: {
        root: null,
        rootMargin: "0px 0px 0px 0px",
        thresholds: 0.5
      }
    };
  },
  methods: {
    goabout(data) {
      console.log("123");
    }
  },

  mounted() {
    $("#home").click(function() {
      console.log(this);

      $("html,body").animate(
        {
          scrollTop: $(".section-home").offset().top
        },
        1000
      );
    });
    $("#about").click(function() {
      $("html,body").animate(
        {
          scrollTop: $(".section-about").offset().top
        },
        1000
      );
    });
    $("#exp").click(function() {
      $("html,body").animate(
        {
          scrollTop: $(".section-exp").offset().top
        },
        1000
      );
    });
    $("#project").click(function() {
      $("html,body").animate(
        {
          scrollTop: $(".section-project").offset().top
        },
        1000
      );
    });
    $("#skill").click(function() {
      $("html,body").animate(
        {
          scrollTop: $(".section-skill").offset().top
        },
        1000
      );
    });
    $("#resume").click(function() {
      $("html,body").animate(
        {
          scrollTop: $(".section-resume").offset().top
        },
        1000
      );
    });
    $(window).scroll(function() {
      const scorll0 = $("#nav-0").offset().top;
      const scorll1 = $("#nav-1").offset().top; //789
      const scorll2 = $("#nav-2").offset().top; //1578
      const scorll3 = $("#nav-3").offset().top; //2367
      const scorll4 = $("#nav-4").offset().top; //3398
      const scorll5 = $("#nav-5").offset().top; //4187
      const scorll6 = $("#nav-6").offset().top; //4976

      let now = $(window).scrollTop();
      // console.log(now);

      if (
        now >= (scorll0 + scorll1) / 2 &&
        now <= (scorll1 + scorll2) / 2 - 1
      ) {
        $(".nav__item").css("background-color", "transparent");
        $("#about").css("background-color", "#f2ab37");
      }
      if (
        now >= (scorll1 + scorll2) / 2 &&
        now <= (scorll2 + scorll3) / 2 - 1
      ) {
        $(".nav__item").css("background-color", "transparent");
        $("#exp").css("background-color", "#f2ab37");
      }
      if (
        now >= (scorll2 + scorll3) / 2 &&
        now <= (scorll3 + scorll4) / 2 - 1
      ) {
        $(".nav__item").css("background-color", "transparent");
        $("#project").css("background-color", "#f2ab37");
      }
      if (
        now >= (scorll3 + scorll4) / 2 &&
        now <= (scorll4 + scorll5) / 2 - 1
      ) {
        $(".nav__item").css("background-color", "transparent");
        $("#skill").css("background-color", "#f2ab37");
      }
      if (
        now >= (scorll4 + scorll5) / 2 &&
        now <= (scorll5 + scorll6) / 2 - 1
      ) {
        $(".nav__item").css("background-color", "transparent");
        $("#resume").css("background-color", "#f2ab37");
      }
      if (now >= (scorll5 + scorll6) / 2) {
        $(".nav__item").css("background-color", "transparent");
        $("#contact").css("background-color", "#f2ab37");
      }
      if (now <= scorll1 / 2) {
        $(".nav__item").css("background-color", "transparent");
      }
    });
    console.log($(window).scrollTop());
  }
};
</script>
<style lang="scss">
</style>


