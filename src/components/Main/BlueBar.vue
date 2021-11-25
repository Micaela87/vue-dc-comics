<template>
    <section>
      <div class="s-container">
        <ul>
          <li v-for="(merch, i) in merchData" :key="i">
            <a href="merch.link">
              <img :src="require('@/assets/img/' + merch.url)" :alt="merch.text" :class="merch.url.includes('svg') ? 'img-svg' : ''">
              <span>{{ merch.text.toUpperCase() }}</span>
            </a>
          </li>
        </ul>
      </div>
    </section>
</template>

<script>

export default {
    name: 'BlueBar',
    data() {
      return {
        merchData: [
          {
            text: 'digital comics',
            url: 'buy-comics-digital-comics.png',
            link: '#'
          },
          {
            text: 'merchandise',
            url: 'buy-comics-merchandise.png',
            link: '#'
          },
          {
            text: 'shop locator',
            url: 'buy-comics-shop-locator.png',
            link: '#'
          },
          {
            text: 'subscriptions',
            url: 'buy-comics-subscriptions.png',
            link: '#'
          },
          {
            text: 'dc power visa',
            url: 'buy-dc-power-visa.svg',
            link: '#'
          }
        ]
      }
    }
}
</script>

<style scoped lang="scss">
    section {
      background-color: #0282f9;
      height: fit-content;
      position: relative;
      z-index: 1;
    }

    .s-container {
      width: 75%;
      margin: 0 auto;
      padding: 4rem 0;
    }

    ul {
      display: flex;
      justify-content: space-between;
      align-items: center;
      list-style-type: none;
    }

    ul li {
      width: 20%;
    }

    ul li a {
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      text-decoration: none;
      font-size: 1.2rem;
      height: 5rem;
    }

    img {
      height: 100%;
    }

    .img-svg {
      width: 25%;
      height: auto;
    }

    span {
      display: inline-block;
      padding: 0 0.9rem;
    }
</style>
