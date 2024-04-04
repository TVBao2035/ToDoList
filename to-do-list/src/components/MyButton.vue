<template>
    <button class="btn" :class="{'danger': danger, 'success':success, 'warning':warning}" >{{ props.name }}</button>
</template>


<script setup>
const props = defineProps({
    name: {
        type: String,
        default: "Click Me"
    }, 
    danger: Boolean,
    warning: Boolean,
    success: Boolean
});
</script>

<style scoped>
    .btn{
        padding: 10px 12px;
        font-weight: 600;
        color:white;
        border: none;
        border-radius: 4px;
        background-color: #409eff;
    }
    .btn:active{
        opacity: 0.8;
    }
    .success{
        background-color: #67c23a;
    }
  
    .danger{
        background-color: #f56c6c;
    }
    .warning{
        background-color: #e6a23c;
    }
</style>
