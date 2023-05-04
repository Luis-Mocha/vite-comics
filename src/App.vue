<script>
  import HeaderComp from './components/HeaderComp.vue';
  import BuyComp from './components/BuyComp.vue';
  import FooterComp from './components/FooterComp.vue';
  import SocialComp from './components/SocialComp.vue';
  import MainComp from './components/MainComp.vue';



  export default{
    name: 'App',
    components: {
      HeaderComp,
      BuyComp,
      FooterComp,
      SocialComp,
      MainComp,
    }
  }

</script>

<template>

  <HeaderComp/>
  <MainComp/>
  <BuyComp/>
  <FooterComp/>
  <SocialComp/>

</template>

<style lang="scss">
  @use './style/main.scss';

</style>
