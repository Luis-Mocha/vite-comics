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
        margin-bottom: 20px ;

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

</style>