<template>
  <section>
    <div class="card">
      <div class="img-box">
        <img :src="card.thumb" :alt="card.series">
      </div>
      
      <h3>{{card.series}}</h3>
    </div>
    
  </section>
</template>

<script>

export default {
  name: 'Card',
  props: {
    card: Object
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';

.card {
  flex-basis: calc(100% / 6);
  margin-right: 20px;
  margin-bottom: 40px;
  .img-box {
    height: 190px;
    overflow-y: hidden;
    margin-bottom: 20px;
  }
  h3 {
    max-width: 190px;
    font-size: 14px;
    font-weight: 400;
    text-transform: uppercase;
    color: #FFF;
  }
}

</style>