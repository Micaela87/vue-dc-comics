<template>
  <section>
      <div class="container container-flex">
        <button>{{ lowerFooterData.sign.toUpperCase() }}</button>
        <div class="container-flex">
          <h3>{{ lowerFooterData.follow.toUpperCase() }}</h3>
          <ul>
            <li v-for="(icon, i) in lowerFooterData.icons" :key="i"><a href="icon.url"><img :src="require('@/assets/img/' + icon.icon + '.png')" alt=""></a></li>
          </ul>
        </div>
      </div>
  </section>
</template>

<script>

export default {
  name: 'LowerFooter',
  data() {
    return {
      lowerFooterData: {
        sign: 'sign-up now!',
        follow: 'follow us',
        icons: [
          {
            name: 'facebook',
            icon: 'footer-facebook',
            url: '#'
          },
          {
            name: 'facebook',
            icon: 'footer-facebook'
          },
          {
            name: 'facebook',
            icon: 'footer-facebook'
          },
          {
            name: 'facebook',
            icon: 'footer-facebook'
          },
          {
            name: 'facebook',
            icon: 'footer-facebook'
          }
        ]
      }
    }
  }
}
</script>

<style scoped lang="scss">
  section {
    background-color: #303030;
    height: 10rem;
    position: relative;
    z-index: 1;
  }

  button {
    color: white;
    font-size: 1.8rem;
    background-color: transparent;
    padding: 1rem 2rem;
    box-shadow: none;
    border: 3px solid #037def;
  }

  h3 {
    font-size: 1.8rem;
    color: #037def;
  }

  ul li {
    display: inline-block;
    margin: 0 1rem;
  }
</style>