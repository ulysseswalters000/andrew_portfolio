<template lang="pug">
  div.home
    Navbar
    Carousel
    AboutBlurb
    Projects
    Footer
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar";
import Carousel from "@/components/Carousel";
import AboutBlurb from "@/components/AboutBlurb";
import Projects from "@/components/Projects";
import Footer from "@/components/Footer";

export default {
  name: "home",
  components: {
    Navbar,
    Carousel,
    AboutBlurb,
    Projects,
    Footer
  }
};
</script>
