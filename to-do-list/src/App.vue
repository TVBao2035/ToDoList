<template>
  <div class="container">
    <div class="block_handle">
      <input type="text" v-model="getData" class="inputField" :class="{'isBlur': isBlur}"  @click="handleClick()" @blur="handleBlur()">
      <button-to-do name="Submit" success v-on:click="addData(data)" class="btn-submit" ></button-to-do>
    </div>
    <my-list :data="data"></my-list>
  </div>
</template>

<script setup>
import ButtonToDo from './components/MyButton.vue';
import MyList from './components/MyList.vue';
import { ref } from 'vue';

const data = ref(['truong', 'van', 'bao']);
const getData = ref("");
var isBlur = ref(false);
const handleBlur = ()=>{
  isBlur.value = !isBlur.value;

}
const handleClick = ()=>{
  isBlur.value = !isBlur.value;
}
const addData = ()=>{
  if(getData.value.trim().length !== 0){
    data.value.push(getData.value);
    getData.value = "";
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
  box-shadow: 0 1px 2px 0 rgba(60,64,67, 0.1), 0px 2px 6px 2px rgba(60,64, 67, 0.2);
  width: 30%;
  box-sizing: border-box;
  padding: 20px;
  text-align: start;
}
.block_handle{
  text-align: center;
}
.btn-submit{
  margin-left: 20px;
}
.inputField{
  height: 30px;
  border: 1px solid #333;
  outline: none;
  box-sizing: border-box;
}
.isBlur{
  border: 2px solid #67c23a;
}
</style>
