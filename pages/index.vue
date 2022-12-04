<template>
  <div class="relative">
    <!-- SideBar -->
    <SideBar></SideBar>

    <!-- Content -->
    <div class="w-4/6 md:w-3/4 float-right px-5 overflow-scroll">
      <About></About>
      <Education></Education>
      <Positions></Positions>
      <Skills></Skills>
      <Projects></Projects>
    </div>
  </div>
</template>

<script>
import "animate.css";
import AOS from "aos";
import "aos/dist/aos.css";
import SideBar from "../components/SideBar.vue";
import About from "../components/About.vue";
import Positions from "../components/Positions.vue";
import Skills from "../components/Skills.vue";
import Projects from "../components/Projects.vue";

export default {
  name: "IndexPage",
  mounted() {
    AOS.init();
  },
  data() {
    return {};
  },
  components: { SideBar, About, Positions, Skills, Projects },
};
</script>

<style>
li {
  @apply p-3;
}

.vcenter {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.portfolio-image {
  width: 550px;
}

html {
  @apply bg-gray-200;
  scroll-behavior: smooth;
}

.slide-enter-active,
.slide-leave-active {
  transition: all 1s ease;
}

.slide-enter-from,
.slide-leave-to {
  width: 0;
}

.slide-enter-to,
.slide-leave-from {
  width: auto;
}
</style>
