<template>
  <div class="card-container">
     <div class="img-container">
         <img :src="card.poster" alt="">
    </div> 
 
    <div class="text-container fc-text-center">
        <h3> {{card.title}} </h3>
        <p> {{card.author}}</p>
        <p>{{card.year}} </p>
    </div>

    
  </div>
</template>

<script>
export default {
 name: 'Card',
 props: {
   card: Object
 }
}
</script>

<style lang="scss" scoped>

  @import "../assets/style/vars.scss";
  @import "../assets/style/generals.scss";
  @import "../assets/style/utilities.scss";

  .card-container{
    // width: calc(20% - 36px);
    width: 180px;
    // height: 300px;
    background-color: #2E3A46;
    margin: 18px;
    padding: 20px;
    transition: all 0.3s
  }

  .card-container:hover{
    transform: scale(1.1, 1.1);
  }

  .img-container{
    width: 100%;
     img{
       max-width: 100%;
       cursor: pointer;
     }
  }

  .text-container{
    margin-top: 10px;
     h3{
       color: white;
       margin-bottom: 8px;
       cursor: pointer;
     }
     p{
       color: #7A7573
     }
  }



</style>