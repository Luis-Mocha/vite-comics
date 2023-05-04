<script>
  import HeaderComp from './components/HeaderComp.vue';
  import BuyComp from './components/BuyComp.vue';
  import FooterComp from './components/FooterComp.vue';
  import SocialComp from './components/SocialComp.vue';


  export default{
    name: 'App',
    components: {
      HeaderComp,
      BuyComp,
      FooterComp,
      SocialComp,
    }
  }

</script>

<template>

  <HeaderComp/>
  <div class="bg-dark py-5">
    <div class="text-light text-center">Content Goes Here</div>
  </div>
  <BuyComp/>
  <FooterComp/>
  <SocialComp/>

</template>

<style lang="scss">
  @use './style/main.scss';

</style>
