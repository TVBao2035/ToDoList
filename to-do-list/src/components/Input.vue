<template>
    <div>
        <input type="text" v-model="value" >
        <Button name="click me" primary="true"  v-on:click="handleJobs"></Button>
        <div class="list_to_do">
            <ul>
                <li  v-for="(x, index) in listJobs" v-bind:key="index">{{ x }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
import Button from './Button.vue';
export default {
    data(){
        return {
            value: "",
            listJobs: [],
        }    
    },
    methods:{
        handleJobs(){
            this.listJobs.push(this.value);
            console.log(this.listJobs)
        }
    },
    components:{
        Button,
    },
    name:'input-data',
    props:{
            
    }
}
</script>

<style scoped>
.list_to_do{
    width: 50%;
}
</style>