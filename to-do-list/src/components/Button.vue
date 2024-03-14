<template>
    <button class="btn" v-bind:class="{primary: primary, warning: warning, success: success, danger: danger}">{{ name }}</button>
</template>

<script>
export default {
    name: "buttonAction",
    props:["name", "primary", "danger", "warning", "success"],
    data(){
        return{
           
        }
    }
}
</script>

<style scoped>
    .btn{
        padding: 5px 10px;
        font-weight: 500;
        font-style:italic;
        color:white;
        border: none;
        border-radius: 8px;
        background-color: #909399;
    }
    .success{
        background-color: #67c23a;
    }
    .primary{
        background-color: #409eff;
    }
    .danger{
        background-color: #f56c6c;
    }
    .warning{
        background-color: #e6a23c;
    }
</style>
