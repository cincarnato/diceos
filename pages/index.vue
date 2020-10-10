<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm10 md10>
      <main-image></main-image>

      <about></about>

      <carousel></carousel>

      <services></services>

      <stats></stats>

      <testimonials></testimonials>

      <contact></contact>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from "~/components/Logo.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";
import About from "~/components/About";
import Services from "~/components/Services";
import MainImage from "~/components/MainImage";
import Contact from "~/components/Contact";
import Testimonials from "~/components/Testimonials";
import Carousel from "~/components/Carousel";

export default {
  components: {
    Carousel,
    Testimonials,
    Contact,
    MainImage,
    Services,
    About,
    Logo,
    VuetifyLogo,
  },
};
</script>
