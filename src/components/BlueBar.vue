<template>
    <section>
      <div class="s-container">
        <ul>
          <li v-for="(merch, i) in merchData" :key="i">
            <a href="merch.link">
              <img :src="require('@/assets/img/' + merch.url + '.png')" alt="merch.text">
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
            url: 'buy-comics-digital-comics',
            link: '#'
          },
          {
            text: 'digital comics',
            url: 'buy-comics-digital-comics',
            link: '#'
          },
          {
            text: 'digital comics',
            url: 'buy-comics-digital-comics',
            link: '#'
          },
          {
            text: 'digital comics',
            url: 'buy-comics-digital-comics',
            link: '#'
          },
          {
            text: 'digital comics',
            url: 'buy-comics-digital-comics',
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

    ul li a {
      display: flex;
      align-items: center;
      color: white;
      text-decoration: none;
      font-size: 1.2rem;
    }

    img {
      width: 30%;
    }

    span {
      display: inline-block;
      padding: 0 0.9rem;
    }
</style>
