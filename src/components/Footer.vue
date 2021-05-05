<template>
  <footer>
      <div class="top">
          <div class="container">
              <div class="left">
                  <div class="col" v-for="(lista, index) in footer" :key="index">
                      <ul >
                          <li>{{lista.title}}</li>
                          <li v-for="(link, index) in lista.links" :key="'-' + index"><a :href="link.link">{{link.name}}</a></li>
                      </ul>
                  </div>
              </div>
              <div class="right">
                  <img src="../assets/img/dc-logo-bg.png" alt="">
              </div>
          </div>
      </div>
      <div class="bottom">
          <div class="container">
              <div class="left">
                  <button>sign-up now!</button>
              </div>
              <div class="right">
                  <ul>
                      <li><a href="#">follow us</a></li>
                      <li v-for="(social, index) in social" :key="'soc-' + index">
                          <a :href="social.link">
                             <img :src="social.logo" :alt="social.social">
                          </a>
                      </li>
                  </ul>
              </div>
          </div>
      </div>
  </footer>
</template>

<script>
import {footer, social} from '../data/footer';

export default {
    name: 'Footer',
    data(){
        return {
            footer,
            social

        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/footer";
</style>