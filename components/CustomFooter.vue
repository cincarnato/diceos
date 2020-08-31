<template>
  <v-footer
    class="justify-center"
    color="#292929"
    height="100"
  >
    <v-flex class="flex-column">
      <div class="title font-weight-light white--text text--lighten-1 text-center">
        Diseño e innovación al servicios de tus proyectos
      </div>
      <div class="title font-weight-light grey--text text--lighten-1 text-center">
        &copy; {{ (new Date()).getFullYear() }} — DICEOS
      </div>
    </v-flex>

  </v-footer>
</template>

<script>
    export default {
        name: "CustomFooter"
    }
</script>

<style scoped>

</style>
