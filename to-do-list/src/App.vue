<template>
  <div class="container">
    <Card titleButton="THAM GIA BUỔI HỌC"
          hour="6"
          minute="00"
          state="Sáng"
          day="14" 
          month="03" 
          year="2024" 
          teacherName="Nguyen Van A"
    >
    </Card>
  </div>
</template>

<script>

import Card from './components/Card.vue';
export default {
  name: 'App',
  data(){
    return{
      size: "50px",
      name: "Vue JS",
      color: 'green',
      className: 'heading_1',
    }
  },
  components: {
   Card
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
  .container{
    margin:200px auto;
  }
  .heading_1{
    color: #ff0000;
    font-size: 30px;
  }
</style>
