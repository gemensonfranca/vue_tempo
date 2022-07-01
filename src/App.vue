<template>
  <v-app id="inspire">

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Projeto Comeia (Tempo)</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <!--  -->
      <FormBusca/>
      <CardTempo/>
    </v-main>
  </v-app>
</template>

<script>

  import CardTempo from './components/CardTempo.vue'
  import FormBusca from './components/FormBusca.vue'

  export default {
    name: 'App',
    components: {
      CardTempo,
      FormBusca
    },
    data: () => ({
      links: [
        'Dashboard',
        'Messages',
        'Profile',
        'Updates',
      ],
    }),
  }
</script>