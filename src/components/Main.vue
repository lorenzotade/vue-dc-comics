<template>
  <main>

    <div class="container">
      <h2>Content goes here</h2>
    </div>
    
  </main>
</template>

<script>
export default {
  name: 'Main',
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars.scss';

  .container {
    background-color: $dark;
    padding-top:60px;
    padding-bottom:60px;
    h2 {
      color: #FFF;
    }
  }
  
</style>