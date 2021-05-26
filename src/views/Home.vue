<template>
<div>
  <Header />
  <Products />
  <Footer />
</div>
</template>

<script>
import Header from '@/components/home/Header'
import Products from '@/components/home/Products'
import Footer from '@/components/home/Footer'

export default {
  components: {
    Header,
    Products,
    Footer
  }
}
</script>
