<script>
    export default{
        name: "FooterComp",
        data(){
            return {
                menuLinks: [
                    {
                        nome: 'characters',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'comics',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'movies',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'tv',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'games',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'collectibles',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'videos',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'fans',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'news',
                        url: '#',
                        current: false
                    },
                    {
                        nome: 'shop',
                        url: '#',
                        current: false
                    },
                ],

                dcLinks: [ 'terms of use', 'privacy policy (new)' , 'ad choices' , 'advertising' , 'jobs', 'subscriptions' , 'talent workshops' , ' CPSC certificates' , ' ratings' , 'shop help', 'contact us']
            }
        }
    }
</script>

<template>
    <footer>
        <div class="container h-100 d-flex justify-content-between">

            <div class="footer-list text-light w-50 py-2">
                <!-- dc-comics -->
                <div>
                    <span>
                        dc-comics
                    </span>
                    <ul>
                        <li v-for="(elem, index) in menuLinks" :key="index">
                            <a :href="elem.url" class="text-capitalize fw-light">
                                {{ elem.nome }}
                            </a>
                        </li>
                    </ul>
                </div>

                <!-- shop -->
                <div>
                    <span>
                        shop
                    </span>
                    <ul class="text-capitalize fw-light">
                        <li>
                            <a href="#">
                                shop DC
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                shop DC collectibles
                            </a>
                        </li>
                    </ul>
                </div>

                <!-- DC -->
                <div>
                    <span>
                        dc
                    </span>
                    <ul>
                        <li v-for="(elem, index) in dcLinks" :key="index">
                            <a href="#" class="text-capitalize fw-light">
                                {{ elem}}
                            </a>
                        </li>
                    </ul>
                </div>

                 <!-- sites-->
                 <div>
                    <span>
                        sites
                    </span>
                    <ul class="text-capitalize fw-light">
                        <li>
                            <a href="#">
                                DC
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                MAD Magazine
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                DC Kids
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                DC Universe
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                DC Power Visa
                            </a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="dc-logo">
            </div>
            
        </div>
    </footer>
    
</template>

<style scoped lang="scss">
    @use '../style/main.scss';
    @use '../style/partials/_mixin.scss' as *; //per poter usare mixin
    @use '../style/partials/variables' as *;

    footer {
        height: 420px;
        background-color: red;
        background-image: url(img/footer-bg.jpg);
        background-size: cover;
        background-position: center;
    }

    .footer-list {
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;

        div {
            margin-top: 10px;
            margin-right: 15px;

            span {
                font-size: 18px;
                line-height: 2;
                font-weight: 800;
                text-transform: uppercase;
            }

            a {
                &:hover{
                    text-decoration: underline;
                }
            }
        }
    }

    .dc-logo {
        width: 50%;
        background-image: url(/img/dc-logo-bg.png) ;
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
    }
 
</style>