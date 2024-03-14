<template>
    <div class="container">
        <div>
            <slot name="content"></slot>
        </div>
       <div class="btn">
            <slot name="button"></slot>
       </div>
    </div>
</template>

<script>



export default {
    name: "cardItems",
    components:{

    },
    props:["day", "month", "year", "hour", "minute", "state" ,"teacherName", "time", "titleButton"],
    
    
}
</script>

<style scoped>
.container{
    box-shadow: 0px 0px 10px 5px rgba(51, 43, 43, 0.2);
    display: flex;
    justify-content: space-between ;
    width: 50%;
    font-weight: 540;
    padding: 10px 15px;
    border-radius: 10px;
}

.btn{
    margin: auto 0;
    display: flex;
    gap: 10px;
}

</style>