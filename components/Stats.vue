<template>
  <section id="stats">
    <v-parallax
      :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
      :src="require('~/assets/img/building.jpg')"
     >
      <v-container fill-height>
        <v-row class="mx-auto">
          <v-col
            v-for="[value, title] of stats"
            :key="title"
            cols="12"
            md="4"
          >
            <div class="text-center">
              <div
                class="display-3 font-weight-black mb-4 grey--text text--darken-4 "
                v-text="value"
              ></div>

              <div
                class="title font-weight-bold  text-uppercase grey--text text--darken-4 "
                v-text="title"
              ></div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-parallax>
  </section>

</template>

<script>
    export default {
        name: "Stats",
      data(){
          return {
            stats: [
              ['50', 'Despliegues'],
              ['124', 'OBRAS'],
              ['24', 'Diseños'],
            ],
          }
      }
    }
</script>

<style scoped>

</style>
