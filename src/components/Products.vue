<template>
  <section class="container">

    <ul>
      <li><a href="#"><img src="../assets/img/buy-comics-digital-comics.png" alt="Digital Comics">Digital Comics</a></li>
      <li><a href="#"><img src="../assets/img/buy-comics-merchandise.png" alt="Digital Comics">Dc Merchandise</a></li>
      <li><a href="#"><img src="../assets/img/buy-comics-subscriptions.png" alt="Digital Comics">Subscription</a></li>
      <li><a href="#"><img src="../assets/img/buy-comics-shop-locator.png" alt="Digital Comics">Comic Shop Locator</a></li>
      <li><a href="#"><img src="../assets/img/buy-dc-power-visa.svg" alt="Digital Comics">Dc Power Visa</a></li>
    </ul>
    
  </section>
</template>

<script>
export default {
  name: 'Products'
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars.scss';

  section {
    background-color: $light-blue;
    padding: 50px 15%;
    ul {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      li {
        margin-right: 10px;
        &:last-child {
          margin-right: 0;
        }
        a {
        display: flex;
        align-items: center;
        text-transform: uppercase;
        color: #FFF;
        font-size: 12px;
      }
      } 
      img {
        height: 50px;
        max-width: 50px;
        margin-right: 15px;
      }
    }
  }
</style>