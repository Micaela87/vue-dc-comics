<template>
    <section>
        <div class="flex-container-column">
            <div v-for="(data, i) in navFooterData" :key="i" class="footer-menu">
                <h3>{{ data.title.toUpperCase() }}</h3>
                <ul>
                    <li v-for="(menuData, k) in data.navMenuData" :key="k">
                        <a href="menuData.url">{{ capitalizeFirstLetter(menuData.text) }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: "UpperFooter",
    data() {
        return {
            navFooterData: [
                {
                    title: 'dc comics',
                    navMenuData: [
                        {
                            text: 'characters',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'comics',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'movies',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'tv',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'games',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'collectibles',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'videos',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'fans',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'news',
                            url: '#',
                            active: false,
                        }            
                    ]
                },
                {
                    title: 'shop',
                    navMenuData: [
                        {
                            text: 'shop dc',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'shop dc collectibles',
                            url: '#',
                            active: false,
                        }           
                    ]
                },
                {
                    title: 'dc',
                    navMenuData: [
                        {
                            text: 'characters',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'comics',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'movies',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'tv',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'games',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'collectibles',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'videos',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'fans',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'news',
                            url: '#',
                            active: false,
                        }         
                    ]
                },
                {
                    title: 'sites',
                    navMenuData: [
                        {
                            text: 'characters',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'comics',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'movies',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'tv',
                            url: '#',
                            active: false,
                        },
                        {
                            text: 'games',
                            url: '#',
                            active: false,
                        }
                    ]
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
    section {
        height: 35rem;
        width: 100%;
    }

    .flex-container-column {
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        height: 100%;
        width: 100%;
    }

    .footer-menu {
        padding: 1rem 0;
    }

    h3 {
        color: white;
        font-size: 1.8rem;
        padding: 1rem 0;
    }

    ul li {
        list-style-type: none;
        line-height: 1.4;
    }

    ul li a {
        text-decoration: none;
        font-size: 1.2rem;
        color: #696355;
    }
</style>