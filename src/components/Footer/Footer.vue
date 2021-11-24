<template>
  <footer>
    <div class="container container-flex">
      <UpperFooter :footerData="menuData"/>
      <img src="../../assets/img/dc-logo-bg.png" alt="dc logo">
    </div>
    <LowerFooter />
  </footer>
</template>

<script>
import UpperFooter from './UpperFooter.vue';
import LowerFooter from './LowerFooter.vue';

export default {
  name: 'Footer',
  components: {
    UpperFooter,
    LowerFooter
  },
  props: {
    menu: Array
  },
  data() {
    return {
      menuData: this.menu
    }
  }
}
</script>

<style scoped lang="scss">
  footer {
    background-image: url('../../assets/img/footer-bg.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    height: 45rem;
  }
</style>
