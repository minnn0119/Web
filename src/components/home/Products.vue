<template>
  <v-container mb-12>
    <v-row>
      <v-col sm="10" offset-sm="1" md="8" offset-md="2">
        <h2>Popular Products <v-btn to="store" color="primary" small text> View all</v-btn></h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col sm="10" offset-sm="1" md="8" offset-md="2">
        <v-row>
          <v-col
            sm="6"
            md="4"
            v-for="(product) in $store.state.products.slide(0,3)"
            :key="product.name"
          >        
          <Item />   
          </v-col>
        </v-row>
      </v-col> 
    </v-row>
  </v-container>
</template>

<script>
import Item from './cards/Item'

export default {
  components: {
    Item
  },
  data() {
    return{}
  },
  methods: {
    addToCart(index, quantity = 1) {
      this.$store.commit('addItemToCart', {ItemId: index, quantity})
      this.$store.commit('updateSnackBar', { show: true})
    }
  }
}
</script>

