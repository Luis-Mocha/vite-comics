<script>
    export default{
        name: "BuyComp",
        data(){
            return {
                buyLinks: [
                    {
                        nome: 'digital comics',
                        imgPath: '/img/buy-comics-digital-comics.png',
                        url: '#',
                    },
                    {
                        nome: 'dc merchandise',
                        imgPath: '/img/buy-comics-merchandise.png',
                        url: '#',
                    },
                    {
                        nome: 'subscription',
                        imgPath: '/img/buy-comics-subscriptions.png',
                        url: '#',
                    },
                    {
                        nome: 'comic shop locator',
                        imgPath: '/img/buy-comics-shop-locator.png',
                        url: '#',
                    },
                    {
                        nome: 'dc power visa',
                        imgPath: '/img/buy-dc-power-visa.svg',
                        url: '#',
                    },
                ]
            }
        }
    }
</script>

<template>
    <div class="BuyComp">
        <div class="container">
            <ul>
                <li v-for="(elem, index) in buyLinks" :key="index">
                    <img :src="elem.imgPath" :alt="elem.nome + ' immagine'">
                    <a :href="elem.url">
                        {{ elem.nome }}
                    </a>
                </li>
                
            </ul>
        </div>
    </div>
    
</template>

<style scoped lang="scss">
    @use '../style/main.scss';
    @use '../style/partials/_mixin.scss' as *; //per poter usare mixin
    @use '../style/partials/variables' as *;

    .BuyComp {
        background-color: $blue-dc;
        color: white;
        padding: 30px 0;
        @include flexAlignItems();

        ul{
            @include flexJustify(space-between);
            flex-wrap: wrap;

            li{
                margin: 10px 0;
                display: flex;
                @include flexAlignItems();

                img {
                    width: 60px;
                    aspect-ratio: 1;
                    object-fit: contain;
                }

                a {
                    text-transform:uppercase;
                    margin-left: 8px;
                }
            }
        }
    }

     
</style>