<template>
  <v-app>
    <v-content>
      <v-toolbar>
        <v-toolbar-icon></v-toolbar-icon>
        <v-toolbar-title> Weather App</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items>
          <v-btn>
            <n-link to="/weather"> Weather App</n-link>
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>


      <transition>
        <nuxt />
      </transition>
      
    </v-content>

  </v-app>
</template>

<script>
  export default {
    
  }
</script>

<style lang="scss" scoped>
a{
  text-decoration: none;
  color:white;
}

</style>