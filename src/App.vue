<template>
  <div class="wrapper">
    
    <Header @selectedGenr="selectedChild"/>

    <Main :sendSelection="selected"/>
    
  </div>
</template>

<script>

import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  },

  data(){
    return{
     selected: "",
    }
   },

   methods:{
    selectedChild(text){
      this.selected = text;
    }
  },
}
</script>

<style lang="scss">

 @import "./assets/style/vars.scss";
 @import "./assets/style/generals.scss";
 @import "./assets/style/utilities.scss";

 .wrapper{
   height: 100vh;
 }
  
</style>
