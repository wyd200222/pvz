<template>
<br><br>
<p>学号：{{ stuId }}</p>
<p>班级：{{ stuInfo.class }}</p>
<p>姓名：{{ stuInfo.name }}</p>
<p>性别：{{ stuDesc.sex }}</p>
<p>电话：{{ stuDesc.tel }}</p>
<p>政治面貌: {{ stuDetail.political }}</p>
<p>出生日期: {{ stuDetail.birth }}</p>
<p>成绩：语文{{ stuScore[0] }}分&nbsp;数学{{ stuScore[1] }}分&nbsp;英语{{ stuScore[2] }}分</p>
<div>
    <button @click="changeId">修改学号</button>
    <button @click="changeInfo">修改班级、姓名</button>
    <button @click="changeDesc">修改性别、电话</button>
    <button @click="changeDetail">修改政治面貌、生日</button>
    <button @click="changeScore">修改成绩</button>
</div>
</template>
<script setup>
    import { ref, reactive, toRef, toRefs } from "vue"
    let stuId = ref('4202350601228')
    const changeId = event => stuId.value="4202350101505"
    let stuInfo = reactive({
        class: "计科2301班",
        name: "王奕达" 
    });
    const changeInfo = event => {
        stuInfo.class= "计科2305班"
        stuInfo.name="张三"
    };
    let stuDesc = reactive({
        sex: "男",
        tel: "13027011279"
    });
    const sex2 = toRef(stuDesc, "sex")
    const tel2 = toRef(stuDesc, "tel")
    const changeDesc = event => {
        sex2.value="女"
        tel2.value="13000000000"
    }
    let stuDetail = reactive({
        political: "共青团员",
        birth: "2002-02-02"
    })
    const stuDetail2 = toRefs(stuDetail)
    const changeDetail = event => {
        stuDetail2.political.value = "群众"
        stuDetail2.birth.value = "2026-04-02"
    };
    let stuScore = reactive([93, 97, 95])
    const changeScore = event => {
        stuScore[0] = 100
        stuScore[1] = 100
        stuScore[2] = 100
    };
</script>
<style>
    button{
        width: auto;
        height: 30px;
        align-self: center;
        margin: 10px;
        display: inline-block;
    }
    p{
        margin: 5px;
        text-align: left;
        margin-left: 400px;
    }
</style>