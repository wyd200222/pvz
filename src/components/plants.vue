<template>
    <div>
        <h1>植&nbsp;&nbsp;&nbsp;&nbsp;物&nbsp;&nbsp;&nbsp;&nbsp;列&nbsp;&nbsp;&nbsp;&nbsp;表</h1>
        <input placeholder="请输入要查询的水果：" v-model="string">
        <ul type="none">
            <li v-for="plant in filterlist" :key="plant.name">
                <p>{{ plant.name }}</p>
                <img :src="plant.img">
            </li> 
        </ul>
    </div>
</template>

<script setup>
    import { computed, ref } from "vue"
    const plantlist = [
        { name: "豌豆射手", img: "/plants/豌豆射手.jpg" },
        { name: "向日葵", img: "/plants/向日葵.jpg" },
        { name: "樱桃炸弹", img: "/plants/樱桃炸弹.jpg" },
        { name: "坚果", img: "/plants/坚果.jpg" },
        { name: "土豆雷", img: "/plants/土豆雷.jpg" },
        { name: "寒冰射手", img: "/plants/寒冰射手.jpg" },
        { name: "大嘴花", img: "/plants/大嘴花.jpg" },
        { name: "双发射手", img: "/plants/双发射手.jpg" },
        { name: "小喷菇", img: "/plants/小喷菇.jpg" },
        { name: "阳光菇", img: "/plants/阳光菇.jpg" },
        { name: "大喷菇", img: "/plants/大喷菇.jpg" },
        { name: "墓碑苔藓", img: "/plants/墓碑苔藓.jpg" },
        { name: "魅惑菇", img: "/plants/魅惑菇.jpg" },
        { name: "胆小菇", img: "/plants/胆小菇.jpg" },
        { name: "寒冰菇", img: "/plants/寒冰菇.jpg" },
        { name: "毁灭菇", img: "/plants/毁灭菇.jpg" },
        { name: "睡莲", img: "/plants/睡莲.jpg" },
        { name: "倭瓜", img: "/plants/倭瓜.jpg" },
        { name: "三线射手", img: "/plants/三线射手.jpg" },
        { name: "海藻", img: "/plants/海藻.jpg" },
        { name: "火爆辣椒", img: "/plants/火爆辣椒.jpg" },
        { name: "地刺", img: "/plants/地刺.jpg" },
        { name: "火炬树桩", img: "/plants/火炬树桩.jpg" },
        { name: "高坚果", img: "/plants/高坚果.jpg" },
        { name: "海蘑菇", img: "/plants/海蘑菇.jpg" },
        { name: "灯笼草", img: "/plants/灯笼草.jpg" },
        { name: "仙人掌", img: "/plants/仙人掌.jpg" },
        { name: "三叶草", img: "/plants/三叶草.jpg" },
        { name: "双向射手", img: "/plants/双向射手.jpg" },
        { name: "杨桃", img: "/plants/杨桃.jpg" },
        { name: "南瓜", img: "/plants/南瓜.jpg" },
        { name: "磁力菇", img: "/plants/磁力菇.jpg" },
        { name: "卷心菜投手", img: "/plants/卷心菜投手.jpg" },
        { name: "花盆", img: "/plants/花盆.jpg" },
        { name: "玉米投手", img: "/plants/玉米投手.jpg" },
        { name: "咖啡豆", img: "/plants/咖啡豆.jpg" },
        { name: "大蒜", img: "/plants/大蒜.jpg" },
        { name: "莴苣保护伞", img: "/plants/莴苣保护伞.jpg" },
        { name: "金盏花", img: "/plants/金盏花.jpg" },
        { name: "西瓜投手", img: "/plants/西瓜投手.jpg" },
        { name: "机枪射手", img: "/plants/机枪射手.jpg" },
        { name: "双生向日葵", img: "/plants/双生向日葵.jpg" },
        { name: "忧郁菇", img: "/plants/忧郁菇.jpg" },
        { name: "猫尾草", img: "/plants/猫尾草.jpg" },
        { name: "冰瓜投手", img: "/plants/冰瓜投手.jpg" },
        { name: "吸金石", img: "/plants/吸金石.jpg" },
        { name: "钢地刺", img: "/plants/钢地刺.jpg" },
        { name: "玉米加农炮", img: "/plants/玉米加农炮.jpg" },
        { name: "变身茄子", img: "/plants/变身茄子.jpg" },
    ]
    const filterlist = computed(() => {
        return plantlist.filter(plant => plant.name.includes(string.value))
    })
    let string = ref("")
</script>

<style>
    ul{
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
        justify-content: center;
        padding: 0;
    }
    img{
        width: 100px;
    }
    input{
        width: 50%;
        display: block;
        margin: 0 auto 20px;
    }
    div{
        width: 90%;
        margin: 30px auto;
        text-align: center;
    }
    h1{
        margin-bottom: 20px;
        font-family: 华文彩云;
        font-weight: bold;
    }
</style>