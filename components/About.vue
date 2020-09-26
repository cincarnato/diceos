<template>
  <section id="about-me">
    <div class="py-12"></div>

    <v-container class="text-center">
      <h2 class="display-2 font-weight-bold mb-3">Nosotros</h2>

      <v-responsive
        class="mx-auto mb-8"
        width="56"
      >
        <v-divider class="mb-1"></v-divider>

        <v-divider></v-divider>
      </v-responsive>

      <v-responsive
        class="mx-auto title font-weight-light mb-8"
        max-width="720"
      >
        Contamos con una larga trayectoria y participacion en la contrucción de escuelas, caminos, espacios verdes, casas y todo tipo de obras civiles.
        Para nosotros cada una de ellas es una obra de arte y representa un nuevo desafio para continuar construyendo nuestro futuro junto a ustedes.
      </v-responsive>

<!--      <v-avatar
        class="elevation-12 mb-12"
        size="128"

      >
        <v-img contain :src="require('~/assets/img/craftsmen.jpg')"></v-img>
      </v-avatar>-->

      <div></div>


    </v-container>

    <div class="py-12"></div>
  </section>
</template>

<script>
    export default {
        name: "About"
    }
</script>

<style scoped>

</style>
