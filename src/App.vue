<template>
  <div id="app">

    <Header />

    <Jumbotron />
    
    <Comics />

    <Main />

    <Footer />

  </div>
</template>

<script>
import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import Comics from './components/Comics.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Comics,
    Main,
    Footer
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');
@import './style/general';
</style>
