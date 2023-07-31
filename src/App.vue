
<template>
  <div id="app"> 
    <v-main-wrapper />
  </div>

</template>

<script>  
  import vMainWrapper from './components/v-main-wrapper.vue';

export default {
    name: 'app',
    components:{
      vMainWrapper
    }
  }
</script>



<style>
  #app{
    
    text-align: center;
    
    margin-top: 10px;
  }
</style>
