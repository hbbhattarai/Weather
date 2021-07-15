<template>
    <v-container>
         <h1 class="display-1 text-center"> Weather App </h1>
      

            <v-flex xs12>
                
                <v-card color="blue-grey darken-2" dark>
                    <v-card-text >
                        This is Card

                    </v-card-text>
                </v-card>
            </v-flex>
            <v-flex xs12 class="mt-4">
                <v-text-field label="Enter City Name" solo>

                </v-text-field>

            </v-flex>
        

    </v-container>
</template>

<script>
    export default {

        data() {
            return {
               city:'Thimphu'
            }
        },
        created:{

            this.$axios
            .$get(`https://api.openweathermap.org/data/2.5/weather?q={ this.city} & appid={be6d37a03674a5ad9fb355ab8b8fd588}`)
            .then(res=> comsole.log(res));
        }
        
    }
</script>

<style lang="scss" scoped>

</style>