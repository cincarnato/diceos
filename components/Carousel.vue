<template>
  <section id="carousel">
    <v-carousel 
    :cycle="true" 
    :interval="4000" 
    :continuous="true"
     delimiter-icon="mdi-minus"
     height="700px"
    >
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
            src: require('~/assets/img/gallery/casa_cons_1.jpg'),
            title: "Desarrollo y Diseño de Vivienda"
          },
          {
            src: require('~/assets/img/gallery/casa_1.jpg'),
            title: "Desarrollo y Diseño de Vivienda"
          },
          {
            src: require('~/assets/img/gallery/enripiado_5.jpg'),
            title: "Enripiado"
          },
          {
            src: require('~/assets/img/gallery/enripiado_4.jpg'),
            title: "Enripiado"
          },
          {
            src: require('~/assets/img/gallery/escuelas_hospitales.png'),
            title: "Escuelas y Hospitales"
          },
          {
            src: require('~/assets/img/gallery/suelo_1.jpg'),
            title: "Asfaltado"
          },
          {
            src: require('~/assets/img/gallery/obras_1.jpg'),
            title: ""
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
