<template>
<div>
  <v-list-item two-line mt-30>
  <v-card
    class="mx-auto"
    max-width="300"
    v-for="malte in tempo" :key="malte.cidade"
  >
    <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title class="text-h5">
          {{ malte.cidade }}-{{ malte.estado }}
        </v-list-item-title>
        <v-list-item-subtitle>{{ malte.clima }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-card-text>
      <v-row align="center">
        <v-col
          class="text-h4"
          cols="6"
        >
          {{ malte.temperatura }}&deg;C
        </v-col>
        <v-col cols="6">
          <v-img
            src="https://cdn.vuetifyjs.com/images/cards/sun.png"
            alt="Sunny image"
            width="92"
          ></v-img>
        </v-col>
      </v-row>
    </v-card-text>

    <v-list class="transparent">
      <v-list-item
        v-for="item in forecast"
        :key="item.day"
      >
        <v-list-item-title>{{ item.day }}</v-list-item-title>

        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-subtitle class="text-right">
          {{ item.temp }}
        </v-list-item-subtitle>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>

  </v-card>
  </v-list-item>
</div>
</template>

<script>

  export default {
    name: 'CardTempo',
    data () {
      return {
        tempo: [
          { cidade: 'Recife', estado: 'PE', temperatura: '45', clima: 'nublado' },
          { cidade: 'Natal', estado: 'RN', temperatura: '30', clima: 'nublado' },
          { cidade: 'João Pessoa', estado: 'PB', temperatura: '27', clima: 'chuvoso' },
          { cidade: 'Fortaleza', estado: 'CE', temperatura: '35', clima: 'ensolarado' },
          { cidade: 'Maceio', estado: 'AL', temperatura: '33', clima: 'nublado' }
        ],
        time: 0,
        forecast: [
          { day: 'Segunda', icon: 'mdi-white-balance-sunny', temp: '24\xB0/12\xB0' },
          { day: 'Terça', icon: 'mdi-white-balance-sunny', temp: '22\xB0/14\xB0' },
          { day: 'Quarta', icon: 'mdi-cloud', temp: '25\xB0/15\xB0' },
          { day: 'Quinta', icon: 'mdi-cloud', temp: '25\xB0/15\xB0' },
          { day: 'Sexta', icon: 'mdi-cloud', temp: '25\xB0/15\xB0' },
        ],
      }
    }
  }

</script>