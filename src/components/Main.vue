<template>
 
    <main class="fc-container fc-flex fc-flex-between fc-flex-wrap">
       
      <Card
      v-for="(card, index) in cards" :key="index"
      :card="card"
      />
    
    </main>
 
</template>

<script>

import axios from 'axios';
import Card from './Card.vue'

export default {
  name: 'Main',
  components:  {
    Card
  },

  data(){
    return{
      cards:[],
      apiURL: 'https://flynn.boolean.careers/exercises/api/array/music'
    }
  },

  methods:{
    getApi(){
      axios.get(this.apiURL)
      .then( r => {
        this.cards = r.data.response;
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