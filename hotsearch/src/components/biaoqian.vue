<template>
    <div id="biapqian">
        <ul id="ul">
            <li :style="{ color: activeindex == index ? 'rgb(88, 143, 226)' : '#000' }" v-for="(item, index) in shuju" @click="dianji(index, item.id)" :key="item.id">
                <span>{{ item.name }}</span> 
            </li>
        </ul>
        <div id="content1" v-show="id == 1">
            <wodedingyue></wodedingyue>
        </div>
        <div id="content2" v-show="id == 2">
            <quanbu></quanbu>
        </div>
        <div id="content3" v-show="id == 3">
            <zonghe></zonghe>
        </div>
        <div id="content4" v-show="id == 4">
            <keji></keji>
        </div>
        <div id="content5" v-show="id == 5">
            <yule></yule>
        </div>
        <div id="content4" v-show="id == 6">
            <shequ></shequ>
        </div>
        <div id="content5" v-show="id == 7">
            <gouwu></gouwu>
        </div>
    </div>
</template>

<script>
import wodedingyue from './wodedingyue.vue'
import zonghe from './zonghe.vue'
import keji from './keji.vue'
import yule from './yule.vue'
import shequ from './shequ.vue'
import gouwu from './gouwu.vue'
import quanbu from './quanbu.vue'
export default {
    name: 'HotsearchBiaoqian',
    components: {
        wodedingyue,
        quanbu,
        zonghe,
        keji,
        yule,
        shequ,
        gouwu,
    },
    data() {
        return {
            id: 1,
            index22:0,
            activeindex: 0,
            shuju:[
                {
                    id:1,
                    name:"我的订阅"
                },
                {
                    id:2,
                    name:"全部"
                },
                {
                    id:3,
                    name:"综合"
                },
                {
                    id:4,
                    name:"科技"
                },
                {
                    id:5,
                    name:"娱乐"
                },
                {
                    id:6,
                    name:"社区"
                },
                {
                    id:7,
                    name:"购物"
                },
            ], 
        };
    },
    methods: {
        dianji(index, id) {
            this.id = id
            this.activeindex = index
        },
    },
};
</script>

<style scoped>
li{
    list-style: none;
    margin-top: 10px;
}
#ul{
    width: 90%;
    height: 8vh;
    line-height: 8vh;
    margin: auto;
    display: flex;
    border-bottom:3px solid rgb(156, 156, 156);
}
#ul li{
    width: 15%;
    height: 100%;
}
/* .span{
    border-top:none;
} */
</style>