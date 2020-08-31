<template>
  <section
    id="testimonials"
  >
    <div class="py-8"></div>

    <v-container class="text-center">
      <h2 class="display-2 font-weight-bold mb-2">Testimonios</h2>

      <v-responsive
        class="mx-auto mb-6"
        width="56"
      >
        <v-divider class="mb-1"></v-divider>

        <v-divider></v-divider>
      </v-responsive>

      <v-row>
        <v-col
          v-for="({who, author, text }, i) in features"
          :key="i"
          cols="12"
          md="6"
        >
          <v-card
            class="py-6 px-3"
            color=""
            flat
          >

            <v-card-text
              class="subtitle-1"
            >
              <v-row>
                <v-col class="flex-grow-0 flex-shrink-0">
                  <v-icon color="orange">mdi-format-quote-open</v-icon>
                </v-col>
                <v-col class="flex-grow-1 flex-shrink-0">
                  {{text}}
                </v-col>
              </v-row>
            </v-card-text>

            <v-card-text
              class="justify-end text-right title font-weight-black text-uppercase pb-0"
              v-text="author"
            ></v-card-text>
            <v-card-text
              class="justify-end text-right title font-weight-light pt-0 "
              v-text="who"
            ></v-card-text>

          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <div class="py-12"></div>
  </section>
</template>

<script>
  export default {
    name: "Testimonials",
    data() {
      return {
        features: [
          {
            author: 'Carlos Gutti',
            who: 'Director de Luminense',
            text: 'Las complejidades y desafíos que DICEOS superó con éxito en nuestro nombre incluyen obstáculos sustanciales en los permisos, apoyo a la coordinación y selección de todos los materiales de diseño y acabado, y la dificultad de integrar estructuras nuevas y existentes.',
          },
          {
            author: 'El hijo de Carlos Gutti',
            who: 'Hijo del director de Luminense',
            text: 'Las complejidades y desafíos que DICEOS superó con éxito en nuestro nombre incluyen obstáculos sustanciales en los permisos, apoyo a la coordinación y selección de todos los materiales de diseño y acabado, y la dificultad de integrar estructuras nuevas y existentes.',
          },

        ],
      }
    }
  }
</script>

<style scoped>

</style>
