<template>
  <div class="cards">
    <div v-for="(card, index) in actions" :key="index" class="card">
      <div class="img">
        <img :src="card.thumb" :alt="card.series">
      </div>
      <h4>{{card.series}}</h4>
    </div>
  </div>
</template>

<script>
import { actions } from '../data/dc-comics';

export default {
    name: 'Cards',
    data(){
      return { 
        actions: actions
      }
    }
}
</script>

<style scoped lang="scss">
@import '../style/cards';
</style>