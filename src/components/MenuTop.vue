<template>
  <v-container>
    <v-app-bar
      :collapse="drawer"
      :collapse-on-scroll="!drawer"
      absolute
      color="pink"
      dark
      scroll-target="#scrolling-techniques-6"
    >
      <v-app-bar-nav-icon @click="menu"></v-app-bar-nav-icon>
      <v-toolbar-title> Clinica NutrIsa</v-toolbar-title>
      <v-icon>mdi-fruit-cherries</v-icon>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <router-link to="/">
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-home</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Inicio</v-list-item-title>
            </v-list-item>
          </router-link>
        
          <router-link to="/agenda">
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-calendar-month-outline</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Agenda</v-list-item-title>
            </v-list-item>
          </router-link>
          <router-link to="/imc">
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-calculator</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Calcular IMC</v-list-item-title>
            </v-list-item>
          </router-link>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </v-container>
</template>
<script>
export default {
  name: "MenuTop",
  data: () => ({
    drawer: false,
    group: null,
  }),
  methods: {
    menu() {
      this.drawer = !this.drawer;
    },
  },
};
</script>
<style scoped>
.link-home {
  color: white !important;
  text-decoration: none;
}
</style>
