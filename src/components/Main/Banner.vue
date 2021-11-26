<template>
  <section>
        <img src="@/assets/img/jumbotron.jpg" alt="banner img">
  </section>
</template>

<script>

export default {
  name: 'Banner'
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
