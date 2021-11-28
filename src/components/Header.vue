<template>

  <header> 
     <img src="../assets/img/spotify-logo.png" alt="logo">
  </header>

</template>

<script>

export default {
 name: 'Header',
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