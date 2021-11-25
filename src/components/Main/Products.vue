<template>
  <div id="app">

  </div>
</template>

<script>

export default {
  name: 'Products',
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
