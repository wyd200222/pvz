<template>
<p>初始的字符串：{{ string }}</p>
<p>反转后的字符串：{{ reverse }}</p>
<div>
    <input placeholder="请输入修改的字符串值" v-model="string">
</div>
</template>

<script setup>
import { ref, computed, watch } from "vue"
let string = ref("hello world")
let reverse = computed( () => {
    return string.value.split("").reverse().join("")
})
watch(string, (newVal, oldVal) => {
    console.log("原值：", oldVal, "新值：", newVal)
});
watch(reverse, (newVal, oldVal) => {
    console.log("原倒序值：", oldVal, "新倒序值：", newVal,)
    console.log("---------------------------------------------------")
})
</script>

<style>
    div{
        width: 30%;
        align-items: center;
    }
</style>
