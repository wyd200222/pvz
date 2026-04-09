<template>
    <p>水果列表</p>
    <ul>
        <li v-for="a in fruit" :key="id">水果编号:{{ a.id }}---水果名称：{{ a.name }}---详细信息：{{ a.desc }}</li>
    </ul>
</template>
<script setup>
    const fruit=[
        {
            id: '1',
            name: '苹果',
            desc: '苹果汁水丰富，可以生津止渴。'
        },
        {
            id: '2',
            name: '柠檬',
            desc: '柠檬具有生津止渴、化痰止咳的功效。'
        }
    ]
</script>
<style>
    li, p{
        text-align: left;
        margin: 10px;
    }
</style>