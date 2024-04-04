<template>
    <ul class="list_items">
        <li class="item" v-for="(e, index) in props.data" :key="index">{{ e }} <span class="icon" v-on:click="handleData(props, index)">+</span></li>
    </ul>
</template>

<script setup>

const handleData = (props, index)=>{
    props.data.splice(index, 1);
}
const props = defineProps({
    data: Array
})
</script>

<style scoped>
.list_items{
    padding: 0;
    list-style: none;
}

.item{
    box-shadow: 0 1px 2px 0 rgba(60,64,67, 0.1), 0px 2px 6px 2px rgba(60,64, 67, 0.2);
    margin: 8px 0;
    box-sizing: border-box;
    padding: 5px 8px;
    display: flex;
    justify-content: space-between;
}
.item:hover{
    box-shadow: 0 1px 2px 0 rgba(0, 255, 115, 0.399), 0px 2px 6px 2px rgba(0, 255, 115, 0.503);

}
.icon{
    rotate: 45deg;
    cursor: pointer;
}
</style>