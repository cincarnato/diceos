<template>
  <section id="services" class="grey lighten-3">
    <div class="py-12"></div>

    <v-container class="text-center">
      <h2 class="display-2 font-weight-bold mb-3">SERVICIOS</h2>

      <v-responsive class="mx-auto mb-12" width="56">
        <v-divider class="mb-1"></v-divider>

        <v-divider></v-divider>
      </v-responsive>

      <v-row>
        <v-col
          v-for="({ icon, title, text, img }, i) in features"
          :key="i"
          cols="12"
          md="4"
        >
          <v-card class="py-12 px-3" color="grey lighten-5" height="500px" flat>
            <v-theme-provider dark>
              <div>
                <v-avatar color="primary" size="88">
                  <v-icon large v-text="icon"></v-icon>
                </v-avatar>
              </div>
            </v-theme-provider>

            <v-card-title
              class="justify-center font-weight-black text-uppercase"
              v-text="title"
            ></v-card-title>

            <v-card-text class="subtitle-1"
              ><b>{{ text }}</b></v-card-text
            >
            <v-img
              v-if="img"
              :src="img"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="250px"
            >
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <div class="py-12"></div>
  </section>
</template>

<script>
export default {
  name: "Services",
  data() {
    return {
      features: [
        {
          icon: "mdi-angle-acute",
          title: "Anteproyecto",
          text:
            "Es la faceta del trabajo en la que se exponen los aspectos fundamentales de las características generales de la obra ya sean funcionales, formales, constructivas o económicas, al objeto de proporcionar una primera imagen global de la misma y establecer un avance de presupuesto.",
          img: "",
        },
        {
          icon: "mdi-cube-outline",
          title: "Proyecto y visualizacion 3d",
          text: "",
          img: require("~/assets/img/gallery/3d.jpg"),
        },
        {
          icon: "mdi-shield-outline",
          title: "Dirección Técnica",
          text:
            "Es la función que el profesional desempeña controlando la fiel interpretación de los planos y de la documentación técnica que forma parte del proyecto y la revisión y extensión de los certificados correspondientes a pagos de la obra en ejecución, inclusive el ajuste final de los insumos.",
          img: "",
        },
        {
          icon: "mdi-store",
          title: "Desarrollo Inmobiliario",
          text: "",
          img: require("~/assets/img/gallery/casa_2.jpg"),
        },
        {
          icon: "mdi-pine-tree",
          title: "Decoración y paisajismo",
          text: "",
          img: require("~/assets/img/gallery/decoracion.jpg"),
        },
        {
          icon: "mdi-cable-data",
          title: "Extendido de fibra optica",
          text: "",
          img: require("~/assets/img/gallery/fibra.jpg"),
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>
