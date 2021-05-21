<template>
  <main>

    <div class="container">
      <h2>Current series</h2>
      <div class="card-container">
        <Card 
          v-for="(comic, index) in comics" :key="index"
          :card="comic"
        />
      </div>
      <a href="#">load more</a>
    </div>
    
  </main>
</template>

<script>
import Card from '@/components/Card.vue'
import comics from '@/assets/data/dc-comics.js'

export default {
  name: 'Main',
  data() {
    return {
      comics
    }
  },
  components: {
    Card
  }
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars.scss';
  @import '../assets/style/mixins.scss';

  .container {
    background-color: $dark;
    padding-top:60px;
    padding-bottom: 30px;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    .card-container {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }
    h2 {
      @include mainText();
      font-size: 18px;
      position: absolute;
      left: 15%;
      top: -20px
    }
    a {
      @include mainText();
      font-size: 14px;
    }
  }
  
</style>