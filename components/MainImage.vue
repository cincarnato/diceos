<template>
  <div class="text-center">
    <v-img :src="require('~/assets/img/plane.jpg')">
      <v-theme-provider>
        <v-container fill-height>
          <v-row
            align="center"
            class="black--text mx-auto"
            justify="center"
          >
            <v-col
              class="primary--text shadow--text text-center"
              cols="12"
              tag="h1"
            >
                    <span
                      :class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
                      class="font-weight-regular"
                    >
                      ... el alma de una obra se sostiene en el tiempo...
                    </span>

              <br>

              <span
                :class="[$vuetify.breakpoint.smAndDown ? 'display-3': 'display-4']"
                class="font-weight-black"
              >
                      DICEOS
                    </span>

            </v-col>

            <v-btn
              class="align-self-end"
              fab
              outlined
              @click="$vuetify.goTo('#about-me')"
            >
              <v-icon>mdi-chevron-double-down</v-icon>
            </v-btn>
          </v-row>
        </v-container>
      </v-theme-provider>


    </v-img>
  </div>
</template>

<script>
  export default {
    name: "MainImage"
  }
</script>

<style scoped>
  .shadow--text {
    text-shadow: 1px 1px #333333;
  }
</style>
