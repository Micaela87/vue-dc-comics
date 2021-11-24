<template>
  <div id="app">
    <Header :menu="navMenuData"/>
    <main>
      <BlueBar />
    </main>
    <Footer :menu="navMenuData"/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer/Footer.vue";
import BlueBar from "./components/BlueBar.vue";

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    BlueBar
  },
  data() {
    return {
          navMenuData: [
              {
                  text: 'characters',
                  url: '#',
                  active: false,
              },
              {
                  text: 'comics',
                  url: '#',
                  active: false,
              },
              {
                  text: 'movies',
                  url: '#',
                  active: false,
              },
              {
                  text: 'tv',
                  url: '#',
                  active: false,
              },
              {
                  text: 'games',
                  url: '#',
                  active: false,
              },
              {
                  text: 'collectibles',
                  url: '#',
                  active: false,
              },
              {
                  text: 'videos',
                  url: '#',
                  active: false,
              },
              {
                  text: 'fans',
                  url: '#',
                  active: false,
              },
              {
                  text: 'news',
                  url: '#',
                  active: false,
              },
              {
                  text: 'shop',
                  url: '#',
                  active: false,
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
