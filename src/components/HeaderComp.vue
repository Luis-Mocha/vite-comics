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
    <header>
        <img src="/img/dc-logo.png" alt="">

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
        display: flex;

        nav {
            display: block;
            width: 100%;

            ul{
                // display: flex;
                // justify-content: space-between;
                @include flexJustify(space-between);

                li {
                    list-style-type: none;
                }
            }
            
        }
    }
     
</style>