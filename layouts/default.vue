<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      color="white"
      app
      temporary
    >
      <v-img
        :src="require('~/assets/img/gallery/menu2.jpg')"
        height="100%"
        style="opacity: 0.9"
        gradient="to top, rgba(0, 0, 0, .5), rgba(0, 0, 0, .5)"
      >
        <v-list dark>
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :to="item.to"
            router
            exact
          >
            <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title v-text="item.title" />
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-img>
    </v-navigation-drawer>

    <v-app-bar dark :clipped-left="clipped" color="#EF6C00" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-avatar
        @click="$vuetify.goTo('#main-image')"
        tile
        size="50"
        width="150"
      >
        <img :src="require('~/assets/img/gallery/logo.jpg')" />
      </v-avatar>
      <v-spacer></v-spacer>
      <v-btn text large @click="$vuetify.goTo('#about-me')"> Nosotros </v-btn>
      <v-btn text large @click="$vuetify.goTo('#carousel')"> Galeria </v-btn>
      <v-btn text large @click="$vuetify.goTo('#services')"> Servicios </v-btn>
      <v-btn text large @click="$vuetify.goTo('#testimonials')">
        Testimonios
      </v-btn>
      <v-btn text large @click="$vuetify.goTo('#contact')"> Contacto </v-btn>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main>

    <custom-footer></custom-footer>
  </v-app>
</template>

<script>
import Footer from "~/components/CustomFooter";
import CustomFooter from "~/components/CustomFooter";
export default {
  components: { CustomFooter, Footer },
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "INICIO",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Servicios",
          to: "#services",
        },
        {
          icon: "mdi-account-box ",
          title: "testimonios",
          to: "#testimonials",
        },
        {
          icon: "mdi-card-account-mail",
          title: "Contacto",
          to: "#contact",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "DICEOS",
    };
  },
};
</script>
