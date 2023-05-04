<script>
  import HeaderComp from './components/HeaderComp.vue';
  import BuyComp from './components/BuyComp.vue'


  export default{
    name: 'App',
    components: {
      HeaderComp,
      BuyComp,
    }
  }

</script>

<template>

  <HeaderComp/>
  <div class="bg-dark py-5">
    <div class="text-light text-center">Content Goes Here</div>
  </div>
  <BuyComp/>

</template>

<style lang="scss">
  @use './style/main.scss';

</style>
