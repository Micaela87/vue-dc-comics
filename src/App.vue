<template>
  <div id="app">
    <Header :menu="navMenuData[0].data"/>
    <main>
      <Banner />
      <Products />
      <BlueBar />
    </main>
    <Footer :menu="navMenuData"/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Banner from "./components/Main/Banner.vue";
import Products from "./components/Main/Products.vue";
import BlueBar from "./components/Main/BlueBar.vue";
import Footer from "./components/Footer.vue";

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    BlueBar,
    Banner,
    Products
  },
  data() {
    return {
          navMenuData: [   
            {
              title: 'dc comics',
              data: [
                  {
                      text: 'characters',
                      url: '#',
                  },
                  {
                      text: 'comics',
                      url: '#'
                  },
                  {
                      text: 'movies',
                      url: '#'
                  },
                  {
                      text: 'tv',
                      url: '#'
                  },
                  {
                      text: 'games',
                      url: '#'
                  },
                  {
                      text: 'collectibles',
                      url: '#'
                  },
                  {
                      text: 'videos',
                      url: '#'
                  },
                  {
                      text: 'fans',
                      url: '#'
                  },
                  {
                      text: 'news',
                      url: '#'
                  },
                  {
                      text: 'shop',
                      url: '#'           
                  }
              ]
          },
          {
              title: 'shop',
              data: [
                  {
                      text: 'shop dc',
                      url: '#',
                  },
                  {
                      text: 'shop dc collectibles',
                      url: '#',
                  }
              ]
          },
          {
              title: 'dc',
              data: [
                  {
                      text: 'term of use',
                      url: '#',
                  },
                  {
                      text: 'privacy policy (new)',
                      url: '#',
                  },
                  {
                      text: 'ad choices',
                      url: '#',
                  },
                  {
                      text: 'advertising',
                      url: '#',
                  },
                  {
                      text: 'jobs',
                      url: '#',
                  },
                  {
                      text: 'subscriptions',
                      url: '#',
                  },
                  {
                      text: 'talent workshops',
                      url: '#',
                  },
                  {
                      text: 'cpsc certificates',
                      url: '#',
                  },
                  {
                      text: 'ratings',
                      url: '#',
                  },
                  {
                      text: 'shop help',
                      url: '#',
                  },
                  {
                      text: 'contact us',
                      url: '#',
                  }        
              ]
          },
          {
              title: 'sites',
              data: [
                  {
                      text: 'dc',
                      url: '#',
                  },
                  {
                      text: 'mad magazine',
                      url: '#',
                  },
                  {
                      text: 'dc kids',
                      url: '#',
                  },
                  {
                      text: 'dc universe',
                      url: '#',
                  },
                  {
                      text: 'dc power visa',
                      url: '#',
                  }
              ]
          }
        ]
      };
  }
}
</script>

<style lang="scss">
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
