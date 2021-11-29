<template>
<div class="select-container">

  <span>Seleziona un genere:</span>
  <select v-model="selected" @change="$emit('sendSelection', selected)">
    <option>Tutti</option>
    <option>Rock</option>
    <option>Pop</option>
    <option>Jazz</option>
    <option>Metal</option>
 </select>

</div>

</template>

<script>

export default {
  name: 'Selection',

   data(){
    return{
      selected: 'Tutti'
    }
  },


}

</script>

<style lang="scss" scoped>

 .select-container{
   padding: 15px;
   select{
     width: 150px;
     height: 30px;
     border: none;
     font-size: 12px;
     border-radius: 3px;
   }
   span{
     margin-right: 6px;
     font-size: 13px;
     color: white;
   }
 }

</style>