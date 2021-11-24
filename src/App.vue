<template>
  <div id="app">
    <Header />
    <main>
      <BlueBar />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import BlueBar from "./components/BlueBar.vue";
import Footer from "./components/Footer/Footer.vue";

export default {
  name: 'App',
  components: {
    Header,
    BlueBar,
    Footer
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
