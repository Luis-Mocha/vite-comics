<script>
    export default{
        name: "SocialComp",
        data(){
            return {
            }
        }
    }
</script>

<template>
    <div class="socialComp">

        <div class="container">
            <button class="signButton">
                sign-up now
            </button>

            <div class="social-list">
                <span>follow us</span>
                <a href="http://" target="_blank" rel="noopener noreferrer">
                    <img src="\img\footer-facebook.png" alt="">
                </a>
                <a href="http://" target="_blank" rel="noopener noreferrer">
                    <img src="\img\footer-twitter.png" alt="">

                </a>
                <a href="http://" target="_blank" rel="noopener noreferrer">
                    <img src="\img\footer-youtube.png" alt="">

                </a>
                <a href="http://" target="_blank" rel="noopener noreferrer">
                    <img src="\img\footer-pinterest.png" alt="">

                </a>
                <a href="http://" target="_blank" rel="noopener noreferrer">
                    <img src="\img\footer-periscope.png" alt="">

                </a>
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
    @use '../style/main.scss';
    @use '../style/partials/_mixin.scss' as *; //per poter usare mixin
    @use '../style/partials/variables' as *;

    .socialComp {
        background-color: rgb(48,48,48);

        div {
            height: 100px;
            @include flexAlignItems();
            justify-content: space-between;

            .social-list {
                color: $blue-dc;
                font-weight: 700;
                text-transform: uppercase;

                a {
                    margin-left: 15px;
                    cursor: pointer;
                }
            }
        }
    }

    .signButton {
       border: 3px solid $blue-dc; 
       padding: 1rem;
       background-color: transparent;

       color: white;
       font-weight: 600;
       text-transform: uppercase;

       &:hover {
        background-color: $blue-dc;
       }
    }
     
</style>