<template>
  <header>
      <div class="container container-flex">
          <img src="@/assets/img/dc-logo.png" alt="dc logo">
          <nav>
              <ul>
                  <li v-for="(data, i) in menu" :key="i">
                    <a href="data.url">{{ data.text.toUpperCase() }}</a>
                  </li>
              </ul>
          </nav>
      </div>
  </header>
</template>

<script>

export default {
  name: 'Header',
  props: {
      menu: Array
  }
}
</script>

<style scoped lang="scss">
    header {
        height: 12rem;
        background-color: white;
    }

    img {
        width: 8%;
    }

        ul li {
        display: inline-block;
        margin: 0 1.2rem;
        padding: 3rem 0;
    }

    a {
        display: block;
        font-size: 1.3rem;
        text-decoration: none;
        color: black;
        font-weight: bold;
        position: relative;
    }

    a::after {
        content: "";
        width: 100%;
        height: 1rem;
        position: absolute;
        top: 5.79rem;
        left: 0;
    }

    a:hover {
        color: #0282f9;
    }

    a:hover::after {
        background-color: #0282f9;
    }
</style>
