<template>
  <div id="app">

    <Header />

    <Jumbotron />
    
    <Main />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap');

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container{
  width: 80%;
  margin: 0 auto;
}

ul li{
  list-style: none;
}

li a{
  text-decoration: none;
}
#app {
  font-family: Roboto, sans-serif;
}
</style>
