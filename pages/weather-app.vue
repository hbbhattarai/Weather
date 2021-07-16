<template>
  <v-container>
    <h1 class="display-1 text-center">Weather App</h1>

    <v-flex xs12>
      <v-card color="blue-grey darken-2" dark>
        <v-card-text>
          <v-layout justify-center> 
            <v-flex>
              <h4>Temperature</h4>
              <h1 class="display-1">{{ weather.name }}</h1>
            </v-flex>
          </v-layout>
        </v-card-text>
      </v-card>
    </v-flex>
    <v-flex xs12 class="mt-4">
      <v-form @submit.prevent="getWeatherInfo">
        <v-text-field
          v-model="city"
          label="Enter City Name"
          solo
        ></v-text-field>
      </v-form>
    </v-flex>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      city: 'London',
      weather: {},
    }
  },
  created() {
    this.getWeatherInfo()
  },
  methods: {
    getWeatherInfo() {
      this.$axios
        .get(
          `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=66804b38bd3b31fdf29ff62dfd5406c8`
        )
        .then(res => (this.weather = res))
    },
  },
}
</script>

<style lang="scss" scoped>
</style>