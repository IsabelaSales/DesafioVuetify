<template>
  <v-app>
    <MenuTop/>
    <div class="conteudo">

    <v-main>
      <router-view />
    </v-main>
    </div>

  </v-app>

</template>
<script>
import MenuTop from './components/MenuTop'
export default {
  components: {
    MenuTop
    }
};
</script>

<style lang="scss">

.conteudo{
  margin-top: 50px;
}
</style>
