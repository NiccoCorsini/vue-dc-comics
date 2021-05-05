<template>
  <div class="container">
      <header>
            <div class="left">
                <a href="#"><img src="../assets/img/dc-logo.png" alt=""></a>
            </div>
            <div class="right">
                <nav>
                    <ul>
                        <li v-for="(link, index) in navLinks" :key="'id' + index"><a @click="activeTab(link)" :class="{active: link.active}" :href="link.link">{{link.name}}</a></li>
                    </ul>
                </nav>
            </div>
          
      </header>
  </div>
</template>

<script>
import { navLinks } from '../data/header'

export default {
    name: 'Header',
    data(){
        return {
            navLinks,
        }
    },
    methods:{
        activeTab(link){
            this.navLinks.forEach(element => {
                element.active = false;
            });
            link.active = true;
        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/header";
</style>