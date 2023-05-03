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
    <header class="container">
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
    @use '../style/partials/variables' as *;

    header{
        @include flexJustify(space-between);
        height: 120px;
        padding: 0;
        
        img {
            height: 100px;
        }

        nav {
            height: 100%;
            
            ul{
                // display: flex;
                // align-items: center;
                @include flexAlignItems();
                height: 100%;

                li {
                    height: 100%;
                    @include flexAlignItems();

                    list-style-type: none;
                    margin-left: 30px;
                    border-bottom: 5px solid transparent;
                    
                    &:hover{
                        color: $blue-dc;
                        border-bottom: 5px solid $blue-dc;
                    }

                    a{
                        text-transform: uppercase;
                        font-weight: 600;
                    }
                }
            }
            
        }
    }
     
</style>