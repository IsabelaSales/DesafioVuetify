<template>
  <v-container class="agenda">
    <h2 class="text-h4 text-center mb-3 mt-5">Agenda Março</h2>
    <TabelaAgenda :clubes="clubesOrdenados"/>
  </v-container>
</template>
<script>
import TabelaAgenda from '../components/TabelaAgenda'
export default {
  name: 'AgendaView',
  data (){
    return {
      agendaMarco: []
    }
  },
  created (){
    fetch('https://hackthon-decola.firebaseio.com/clubes-lista.json')
    .then(Response => Response.json())
    .then(json =>{
      this.agendaMarco = json;
      console.log(this.agendaMarco)
    })
  },
  components: {
    TabelaAgenda
  },
  computed: {
    clubesOrdenados() {
      const listaComputada = this.agendaMarco.slice(0).sort((a, b) =>  a.pontos > b.pontos ? -1 : 1);
      return listaComputada;
    }
  }
}
</script>
<style scoped>

</style>