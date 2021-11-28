<template> 
 
    <main class="fc-container fc-flex fc-flex-justify-center">
      <div class="fc-container fc-flex fc-flex-justify-center fc-flex-wrap" v-if="loaded">
         <Card
          v-for="(card, index) in cards" :key="index"
          :card="card"
         />
      </div>
     
     <Loader v-else/>
    
    </main>
 
</template>

<script>

import axios from 'axios';
import Card from './Card.vue'
import Loader from './Loader.vue'

export default {
  name: 'Main',
  components:  {
    Card,
    Loader
  },

  data(){
    return{
      cards:[],
      loaded: false,
      apiURL: 'https://flynn.boolean.careers/exercises/api/array/music'
    }
  },

  methods:{
    getApi(){
      axios.get(this.apiURL)
      .then( r => {
        this.cards = r.data.response;
        this.loaded = true;
        console.log(this.cards);
      })
      .catch( e => {
        console.log(e);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}
</script>

<style lang="scss" scoped>

  @import "../assets/style/vars.scss";
  @import "../assets/style/generals.scss";
  @import "../assets/style/utilities.scss";

  .fc-container{
    margin-top: 50px;
  }

</style>