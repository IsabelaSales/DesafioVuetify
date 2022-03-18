<template>
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="peso"
      :counter="10"
      :rules="nameRules"
      label="Peso"
      required
    ></v-text-field>

    <v-text-field
      v-model="altura"
      :rules="emailRules"
      label="Altura"
      required
    ></v-text-field>


    <v-btn
      color="error"
      class="mr-4"
      @click="calculandoImc"
    >
      Calcular
    </v-btn>

  </v-form>
</template>
<script>
export default {
    name:'FormularioIMC',
    data(){
        return{
            peso: 0,
            altura: 0
        }
    },
    methods:{
        calculandoImc(){
           let alturaQuadrado = this.altura * this.altura
           let imcTotal = (this.peso / alturaQuadrado)
           alert(`Seu IMC É: ${imcTotal}`)
           return imcTotal
        }
    }
}
</script>
<style scoped>

</style>