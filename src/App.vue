<template>
  <div id="app">

    <Header />
    <Main />
    <Products />
    <Footer />
    
  </div>
</template>

<script>

import Header from '@/components/Header.vue';
import Main from '@/components/Main.vue';
import Products from '@/components/Products.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Products,
    Footer
  }
}

</script>

<style lang="scss">

  @import 'assets/style/utilities.scss';
  @import 'assets/style/general.scss';

</style>
