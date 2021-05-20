<template>
  <footer>

    <div class="products container">

    </div> <!-- /products -->

    <div class="top container">

      <div class="nav-columns">

        <div class="col">
          <div class="dc-comics-nav">
            <h3>Dc Comics</h3>
            <ul>
              <li v-for="(link, index) in comics" :key="index"><a href="link.url">{{link.text}}</a></li>
            </ul>
          </div>
          <div class="shop-nav">
            <h3>Shop</h3>
            <ul>
              <li v-for="(link, index) in shop" :key="index"><a href="link.url">{{link.text}}</a></li>
            </ul>
          </div>
          
        </div> <!-- /col I -->

        <div class="col">
          <div class="dc">
            <h3>Dc</h3>
            <ul>
              <li v-for="(link, index) in dc" :key="index"><a href="link.url">{{link.text}}</a></li>
            </ul>
          </div>
        </div> <!-- /col II -->

        <div class="col">
          <div class="dc">
            <h3>Sites</h3>
            <ul>
              <li v-for="(link, index) in sites" :key="index"><a href="link.url">{{link.text}}</a></li>
            </ul>
          </div>
        </div> <!-- /col III -->

      </div> <!-- /nav-columns -->

      <img src="../assets/img/dc-logo-bg.png" alt="Logo">

    </div> <!-- /top-container -->

    <div class="bottom container">
      <a id="sign-up" href="#">Sign-up now!</a>

      <div class="social-list">
        <ul>
          <li><a href="#">Follow us</a></li>
          <li><a href="#"><img src="../assets/img/footer-facebook.png" alt="Facebook"></a></li>
          <li><a href="#"><img src="../assets/img/footer-twitter.png" alt="Twitter"></a></li>
          <li><a href="#"><img src="../assets/img/footer-youtube.png" alt="YouTube"></a></li>
          <li><a href="#"><img src="../assets/img/footer-pinterest.png" alt="Pinterest"></a></li>
          <li><a href="#"><img src="../assets/img/footer-periscope.png" alt="Periscope"></a></li>
        </ul>
      </div>
    </div> <!-- /bottom-container -->

  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      comics: [
        {
          text: 'Characters',
          url: '#'
        },
        {
          text: 'Comics',
          url: '#'
        },
        {
          text: 'Movies',
          url: '#'
        },
        {
          text: 'TV',
          url: '#'
        },
        {
          text: 'Games',
          url: '#'
        },
        {
          text: 'Videos',
          url: '#'
        },
        {
          text: 'News',
          url: '#'
        },
      ],
      shop: [
        {
          text: 'Shop DC',
          url: '#'
        },
        {
          text: 'Shop DC Collectibles',
          url: '#'
        },
      ],
      dc: [
        {
          text: 'Term Of Use',
          url: '#'
        },
        {
          text: 'Privacy Policy (New)',
          url: '#'
        },
        {
          text: 'Ad Choices',
          url: '#'
        },
        {
          text: 'Advertising',
          url: '#'
        },
        {
          text: 'Jobs',
          url: '#'
        },
        {
          text: 'Subscriptions',
          url: '#'
        },
        {
          text: 'Talent Workshops',
          url: '#'
        },
        {
          text: 'CPSC Certificates',
          url: '#'
        },
        {
          text: 'Ratings',
          url: '#'
        },
        {
          text: 'Shop Help',
          url: '#'
        },
        {
          text: 'Contact Us',
          url: '#'
        },
      ],
      sites: [
        {
          text: 'DC',
          url: '#'
        },
        {
          text: 'MAD Magazine',
          url: '#'
        },
        {
          text: 'DC Kids',
          url: '#'
        },
        {
          text: 'DC Universe',
          url: '#'
        },
        {
          text: 'DC Power Visa',
          url: '#'
        },
      ],
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';

  .top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    overflow: hidden;
    img {
      height: 400px;
      transform: scale(1.5);
    }
    .nav-columns {
      display: flex;
      .col {
        margin-right: 30px;
        .dc-comics-nav {
          margin-bottom: 20px;
        }
      }
      h3 {
        color: #FFF;
        font-size: 16px;
        text-transform: uppercase;
        margin-bottom: 20px;
      }
      li {
        padding: 3px 0;
      }
      a {
        color: $footer-links;
        font-size: 12px;
        &:hover {
          color: #FFF;
        }
      }
    }
  }

  .bottom {
    height: 100px;
    background-color: #303030;
    display: flex;
    justify-content: space-between;
    align-items: center;
    a {
      text-transform: uppercase;
    }
    #sign-up {
      color: #FFF;
      display: inline-block;
      padding: 10px;
      border: 2px solid $light-blue;
      font-weight: 600;
      &:hover {
        transform: scale(1.1);
      }
    }
    ul {
      display: flex;
      align-items: center;
      li {
        margin-left: 20px;
        a {
          font-weight: 800;
          color: $light-blue;
        }
        img {
          height: 30px;
        }
      }
    }
  }
</style>