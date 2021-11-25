<template>
    <div class="card">
        <div class="img-container">
            <img :src="details.thumb" :alt="details.series">
        </div>
        <span>{{ details.series.toUpperCase() }}</span>
    </div>
</template>

<script>

export default {
  name: 'ProductCard',
  props: {
      details: Object
  }
}
</script>

<style scoped lang="scss">
    .card {
        width: calc(100% / 6);
        height: fit-content;
        padding: 1rem;
    }

    .img-container {
        height: 20rem;
        width: 100%;
        overflow: hidden;
    }

    img {
        width: 100%;
        height: auto;
    }

    span {
        display: block;
        color: white;
        font-size: 1.2rem;
        padding: 1rem 0;
    }
</style>
