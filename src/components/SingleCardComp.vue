<script>
    export default{
        name: "SingleCardComp",
        //richiamo i props
        props: ['dettagliComic'],
        // altro metodo:
        // props: {
        //     dettagliComic: Object
        // },
        data(){
            return {
                
            }
        }
    }
</script>

<template>

    <div class="comic-card">
        <img :src="dettagliComic.thumb" alt="">
        <div class="cardTitle">{{dettagliComic.series}}</div>
    </div>

</template>

<style scoped lang="scss">
    @use '../style/main.scss';
    @use '../style/partials/_mixin.scss' as *; //per poter usare mixin
    @use '../style/partials/variables' as *;

    .comic-card {
        color: white;
        width: calc(100% / 6 - 15px );
        margin-bottom: 30px ;

        img {
            display: block;
            width: 200px;
            height: 200px;
            object-fit: cover;
        }

        .cardTitle {
            padding: 5px 0;
            font-size: 15px;
            text-transform: uppercase;
        }
    }
    .comic-card {
        @media screen and (max-width: 1000px ){
            width: calc(100% / 4 - 15px );
        }
        @media screen and (max-width: 768px ){
            width: calc(100% / 3 - 15px );
        }
        @media screen and (max-width: 576px ){
            width: calc(100% / 2 - 10px );
        }
    }

</style>