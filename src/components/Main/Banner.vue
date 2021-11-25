<template>
  <section>
        <img :src="require('@/assets/img/' + bannerData[0].url)" :alt="bannerData[0].text">
        <span>{{ seriesData[0].text.toUpperCase() }}</span>
  </section>
</template>

<script>

export default {
  name: 'Banner',
  data() {
    return {
          bannerData: [
              {
                  text: 'banner img 1',
                  url: 'jumbotron.jpg'
              }      
          ],
          seriesData: [
              {
                  text: 'current series'
              }
          ]
      };
  }
}
</script>

<style scoped lang="scss">
    section {
        height: 32rem;
        overflow: hidden;
        position: relative;
    }

    img {
        width: 100%;
    }

    span {
        display: block;
        color: white;
        font-size: 2rem;
        background-color: #0282f9;
        padding: 1rem 2rem;
        position: absolute;
        bottom: -2.2rem;
        left: 15rem;
        z-index: 1;
    }
</style>
