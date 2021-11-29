<template>

  <header class="fc-flex fc-flex-between fc-flex-align-center"> 
     <img src="../assets/img/spotify-logo.png" alt="logo">
     <Selection @sendSelection="getGen"/>
  </header>

</template>

<script>

import Selection from './Selection.vue'

export default {
 name: 'Header',
 
 components: {
   Selection
 },

 data(){
    return{
      selection : "",
    }
  },

 methods:{
   getGen(text){
      this.selection = text;
      return this.$emit("selectedGenr",this.selection);
    }
  },

}
</script>

<style lang="scss" scoped>

  @import "../assets/style/vars.scss";
  @import "../assets/style/generals.scss";
  @import "../assets/style/utilities.scss";
  
  header{
    height: 60px;
    background-color: #2E3A46;
     img{
       height: 100%;
       padding: 10px;
       cursor: pointer;
       margin-left: 5px;
     }
  }
 
</style>