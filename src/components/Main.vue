<template>
  <main>
      <div class="container">
          <ul>
              <li v-for="(link, index) in navLinks" :key="'id' + index"><a href="#">
                  <img :src="link.logo">
                  {{link.name}}
                  </a></li>
          </ul>
      </div>
  </main>
</template>

<script>
import {navLinks} from '../data/main-sec';

export default {
    name: 'Header',
    data(){
        return {
            navLinks,
        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/main";
</style>