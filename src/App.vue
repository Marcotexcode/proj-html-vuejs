<template>

  <div id="app">
    
    <div class="container--head-jumbo">

      <Header/>

      <Jumbotron/>

    </div>

    <Main/>

    <Footer/>

  </div>

</template>


<script>

import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {

  name: 'App',

  components: {

    Header,
    Jumbotron,
    Main,
    Footer

  }

}

</script>


<style lang="scss">

  @import '@/style/commons.scss';
  @import '@/style/variabili.scss';
  @import '@/style/mixins.scss';

  .container--head-jumbo {
    background-image: url("./assets/img/header-image-homepage.jpg");
    @include backgroundImg ();
    height: 700px;
  }


</style>
