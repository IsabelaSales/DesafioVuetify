<template>
    <v-container>
            <h2 class="text-h4 text-center mb-3 mt-5">CALCULAR IMC</h2>
            <FormularioIMC/>
    </v-container>
</template>
<script>
import FormularioIMC from '../components/FormularioIMC'
export default {
    name: 'CalculandoIMCView',
    components:{
        FormularioIMC,
    }
}
</script>
<style scoped>

</style>