<template>

  <v-sheet 
    height="sheetHeight"
  >
    <v-container class="fill-height">
      <v-row
        aligh="center"
        justify="center"
      > 
        <h1 class="text-center display-3 hidden-xs-only">
          Welcome to My Shop!!!
        </h1>
        <h1 class="text-center display-1 hidden-sm-and-up">
          Welcome to My Shop!!!
        </h1>
      </v-row>
    </v-container>
  </v-sheet>
</template>

<script>
module.exports = {
  computed: {
    sheetHeight(){
        switch (this.vuetify.breakpoint.name) {
          case 'xs': return '220px'
          case 'sm': return '400px'
          case 'md': return '500px'
          case 'lg': return '600px'
          case 'xl': return '800px'
        }
        return'300ps'
      }
    }
  }


</script>