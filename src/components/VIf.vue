<template>
    <p>小明的学习评定等级为：</p>
    <p v-if="flag===2">优秀</p>
    <p v-else-if="flag===1">良好</p>
    <p v-else="flag===0">差</p>
    <div>
        <button @click="flag=2">切换成优秀</button>
        <button @click="flag=1">切换成良好</button>
        <button @click="flag=0">切换成差</button>       
    </div>
</template>
<script setup>
    import { ref } from "vue"
    let flag = ref(1)
</script>
<style>
    p{
        margin-left: 10px;
    }
    *{
        text-align: left;
    }
    button{
        display: inline-block;
        margin: 0;
        border-color: white;
    }
    div{
        margin-left: 10px;
    }
</style>
