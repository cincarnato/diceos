<template>
  <section id="carousel">
    <v-carousel :cycle="true" :interval="4000" :continuous="true">
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="display-3 font-weight-bold white--text shadow--text">{{ item.title }}</div>
        </v-row>

      </v-carousel-item>
    </v-carousel>
  </section>
</template>

<script>
  export default {
    name: "Carousel",
    data() {
      return {
        items: [
          {
            src: require('~/assets/img/gallery/desarrollo_disenio_vivienda_1.png'),
            title: "Desarrollo y Diseño de Vivienda"
          },
          {
            src: require('~/assets/img/gallery/desarrollo_disenio_vivienda_2.png'),
            title: "Desarrollo y Diseño de Vivienda"
          },
          {
            src: require('~/assets/img/gallery/enripiado_2.png'),
            title: "Enripiado"
          },
          {
            src: require('~/assets/img/gallery/enripiado_1.png'),
            title: "Enripiado"
          },
          {
            src: require('~/assets/img/gallery/escuelas_hospitales.png'),
            title: "Escuelas y Hospitales"
          },
          {
            src: require('~/assets/img/gallery/perfilado_suelo.png'),
            title: "Perfilado del suelo"
          },
          {
            src: require('~/assets/img/gallery/viales_excavaciones.png'),
            title: "Nivelacion vial y excavaciones"
          },
          {
            src: require('~/assets/img/gallery/cubiertas_metalicas.png'),
            title: "Cubiertas Metalicas"
          },
        ],
      }
    },
  }
</script>

<style scoped>
  .shadow--text {
    text-shadow: 1px 1px #333333;
  }
</style>
