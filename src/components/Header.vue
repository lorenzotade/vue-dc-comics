<template>
  <header>

    <div class="container">

      <a href="/"><img src="../assets/img/dc-logo.png" alt="Logo"></a>

      <ul>
        <li 
          v-for="(link, index) in links" 
          :key="index"
          :class="{'active': link.current === true}"
          @click="setActive(index)"
        >
          <a :href="link.url">{{link.text}}</a>
        </li>
      </ul>
      
    </div> <!-- /end container -->

  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      links: [
        {
          text: 'Charachters',
          url: 'javascript:void(0)',
          current: true
        },
        {
          text: 'Comics',
          url: 'javascript:void(0)',
          current: false
        },
        {
          text: 'Movies',
          url: 'javascript:void(0)',
          current: false
        },
        {
          text: 'Tv',
          url: '#',
          current: false
        },
        {
          text: 'Games',
          url: '#',
          current: false
        },
        {
          text: 'Collectibles',
          url: '#',
          current: false
        },
        {
          text: 'Videos',
          url: '#',
          current: false
        },
        {
          text: 'Fans',
          url: '#',
          current: false
        },
        {
          text: 'News',
          url: '#',
          current: false
        },
        {
          text: 'Shop',
          url: '#',
          current: false
        }
      ]
    }
  },
  methods: {
    setActive(index) {
      this.links.forEach((link) => {
        link.current = false;
      })
      this.links[index].current = true
    }
  }
}
</script>

<style lang="scss" scoped>

  @import '../assets/style/vars.scss';

  .container {
    display: flex;
    height: 100%;
    justify-content: space-between;
    align-items: center;
    img {
      height: 70px;
    }
    ul {
      display: flex;
      height: 100%;
      li {
        margin: 0 10px;
        &.active {
          color: $light-blue;
          border-bottom: 4px solid $light-blue;
        }
      }
      a {
        display: inline-block;
        color: $dark;
        text-transform: uppercase;
        font-weight: 600;
        font-size: 11px;
        line-height: 100px;
      }
    }
  }
</style>