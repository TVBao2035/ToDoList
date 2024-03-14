<template>
  <div class="container">
    <Card>
      <template #content>
          <ul class="list-item">
            <li class="item">Ngày {{ day }} tháng {{ month }} năm {{ year }}</li>
            <li class="item teacher-name">Giảng viên:{{ teacherName }}</li>
            <li class="item">{{ state }} {{ hour }}:{{ minute }}</li>
          </ul>
      </template>
     
      <template #button>
        <Button :name="titleButton" primary="true"></Button>
      </template>
    </Card>
  </div>
</template>

<script>

import Card from './components/Card.vue';
import Button from './components/Button.vue';


export default {
  name: 'App',
  data(){
    return{
      day: "14",
      month: "03",
      year: "2024",
      hour: "06",
      minute: "00",
      state: "Sáng",
      teacherName: "Nguyen Van A",
      titleButton: "THAM GIA BUOI HOC"
    }
  },
  components: {
   Card, Button,
  }
}
</script>

<style>
.list-item{
    list-style: none;
    padding: 0;
}
.item{
    margin-bottom: 10px;
}
.teacher-name{
    color: red;
}
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
