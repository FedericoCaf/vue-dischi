<template>
  <main>
    <div class="fc-container fc-flex fc-flex-between fc-flex-wrap">
       
      <Card/>
      <Card/>
      <Card/>
      <Card/>
      <Card/>
      <Card/>
      <Card/>
      <Card/>
      <Card/>
      <Card/>

    </div>
  </main>
</template>

<script>

import Card from './Card.vue'

export default {
  name: 'Main',
  components:  {
    Card
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