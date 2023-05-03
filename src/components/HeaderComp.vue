<script>
    export default{
        name: "HeaderComp",
        data(){
            return {
                menuLinks: [
                    {
                        nome: 'characters',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'comics',
                        url: '/',
                        current: true
                    },
                    {
                        nome: 'movies',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'tv',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'games',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'collectibles',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'videos',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'fans',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'news',
                        url: '/',
                        current: false
                    },
                    {
                        nome: 'shop',
                        url: '/',
                        current: false
                    },
                ]
            }
        }
    }
</script>

<template>
    <header class="bg-danger container">
        <div class="logo">
            <img src="/img/dc-logo.png" alt="">
        </div>
        

        <nav>
            <ul>
                <li v-for="(elem, index) in menuLinks" :key="index">
                    <a :class="( elem.current === true ) ? 'active' : '' " href="">
                        {{ elem.nome }}
                    </a>
                </li>
                
            </ul>
        </nav>
    </header>
</template>

<style scoped lang="scss">
    // @use '../style/main.scss';
    @use '../style/partials/_mixin.scss' as *; //per poter usare mixin

    header{
        @include flexJustify(space-between);
        height: 120px;
        padding: 0;

        .logo {
            img {
                height: 80px;
            }
        }

        nav {
            height: 100%;
            display: flex;
            align-items: center;
            
            ul{
                display: flex;

                li {
                    list-style-type: none;
                    margin-left: 30px;

                    a{
                        text-transform: uppercase;
                        font-weight: 600;
                    }
                }
            }
            
        }
    }
     
</style>