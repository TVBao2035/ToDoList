<template>
    <div class="container">
        <ul class="list-item">
            <li class="item">Ngày {{ day }} tháng {{ month }} năm {{ year }}</li>
            <li class="item teacher-name">Giảng viên:{{ teacherName }}</li>
            <li class="item">{{ state }} {{ hour }}:{{ minute }}</li>
        </ul>
        <Button class="btn" :name="titleButton" primary="true"></Button>
    </div>
</template>

<script>
import Button from './Button.vue';
export default {
    name: "cardItems",
    components:{
        Button,
    },
    props:["day", "month", "year", "hour", "minute", "state" ,"teacherName", "time", "titleButton"]
    
}
</script>

<style scoped>
.container{
    box-shadow: 0px 0px 10px 5px rgba(51, 43, 43, 0.2);
    display: flex;
    justify-content: space-between;
    width: 50%;
    font-weight: 540;
    padding: 10px 15px;
    border-radius: 10px;
}
.list-item{
    list-style: none;
    padding: 0;
}
.item{
    margin-bottom: 10px;
}

.btn{
    margin: auto 0;
}
.teacher-name{
    color: red;
}
</style>