<template>
  <footer>
    <BlueBar />
    <!-- upper footer -->
    <section id="upper-footer">
      <div class="container container-flex">
        <div class="menu-container">
          <div class="flex-container-column">
              <div v-for="(data, i) in menu" :key="i" class="footer-menu">
                  <h3>{{ data.title.toUpperCase() }}</h3>
                  <ul>
                      <li v-for="(menuData, k) in data.data" :key="k">
                          <a href="menuData.url">{{ capitalizeFirstLetter(menuData.text) }}</a>
                      </li>
                  </ul>
              </div>
          </div>
        </div>
        <img src="../assets/img/dc-logo-bg.png" alt="dc logo">
      </div>
    </section>
    <!-- lower footer -->
    <section id="lower-footer">
      <div class="container container-flex">
        <button>SIGN UP NOW!</button>
        <div class="container-flex">
          <h3>FOLLOW US</h3>
          <ul>
            <li v-for="(icon, i) in icons" :key="i">
              <a href="icon.url"><img :src="require('@/assets/img/' + icon.icon + '.png')" :alt="icon.name"></a>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </footer>
</template>

<script>
import BlueBar from "./Main/BlueBar.vue";

export default {
  name: 'Footer',
  components: {
    BlueBar
  },
  props: {
    menu: Array
  },
  data() {
        return {
          icons: [
            {
              name: 'facebook',
              icon: 'footer-facebook',
              url: '#'
            },
            {
              name: 'periscope',
              icon: 'footer-periscope'
            },
            {
              name: 'pinterest',
              icon: 'footer-pinterest'
            },
            {
              name: 'twitter',
              icon: 'footer-twitter'
            },
            {
              name: 'youtube',
              icon: 'footer-youtube'
            }
          ]
      };
    },
    methods: {
        capitalizeFirstLetter(string) {
            let arrString = string.split(' ');

            let arrResult = [];
            
            for (let i = 0; i < arrString.length; i++) {

                let string = arrString[i].toLowerCase();

                arrResult.push(string.charAt(0).toUpperCase() + string.slice(1));
            }

            let result = arrResult.join(' ');

            return result;
        }
    },
}
</script>

<style scoped lang="scss">
// upper footer
  #upper-footer {
    background-image: url('../assets/img/footer-bg.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    height: 35rem;
  }

  .menu-container {
    height: 100%;
  }
  .flex-container-column {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      height: 100%;
      width: 100%;
      padding: 1rem 0;
  }

  .footer-menu {
      padding: 1rem;
  }

  #upper-footer h3 {
      color: white;
      font-size: 1.8rem;
      padding: 1rem 0;
  }

  #upper-footer ul li {
      list-style-type: none;
      line-height: 1.4;
  }

  #upper-footer ul li a {
      text-decoration: none;
      font-size: 1.2rem;
      color: #696355;
  }

// lower footer
  #lower-footer {
    background-color: #303030;
    height: 10rem;
    position: relative;
    z-index: 1;
  }

  #lower-footer button {
    color: white;
    font-size: 1.8rem;
    background-color: transparent;
    padding: 1rem 2rem;
    box-shadow: none;
    border: 3px solid #037def;
    cursor: pointer;
  }

  #lower-footer h3 {
    font-size: 1.8rem;
    color: #037def;
  }

  #lower-footer ul li {
    display: inline-block;
    margin: 0 1rem;
  }
</style>
