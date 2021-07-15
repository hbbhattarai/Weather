<template>
  <v-app>
    <v-content>
      <v-toolbar color="indigo" dark>
        <v-toolbar-side-icon></v-toolbar-side-icon>
        <v-toolbar-title>Learing Nuxt</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn flat>
            <n-link to="/weather-app">Weather App</n-link>
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    
    <transition>
      <nuxt />
    </transition>
    </v-content>
  </v-app>
</template>

<style scoped>
a{
  text-decoration: none;
  color:white;
}
</style>