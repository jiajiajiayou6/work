<template>
    <div>
        <div class="zong1">
                <div class="left">
                    <ul class="valere">
                        <li><input type="text" class="sousuo" placeholder="搜索" name="" id=""></li>
                        <li class="liqq" :style="{ background: index22 == index ? 'rgb(88, 143, 226)' : '' }" v-for="(item, index) in dingyue"  :key="item.id" @click="dianji1(index, item.id)"> 
                            <img class="qqw1" :src="item.img">
                            <span class="qqw5">{{ item.title }}</span>
                        </li>
                    </ul>
                </div>
                <div class="right">
                    <ul class="valere2">
                        <li v-show="index22 == 0" v-for="item in data1"  :key="item.title">
                           <span class="qw4" :class="`${item.index==1 ? 'qqw4' : ''}${item.index==2 ? 'qqqw4' : ''}${item.index==3 ? 'qqqqw4' : ''}`">{{ item.index }}</span>
                           <span class="qqw5"> {{ item.title}}</span>
                           <span class="qqw6">{{ item.hotValue }}</span>
                        </li>
                          <li v-show="index22 == 1" v-for="item  in data2"   :key="item.hotValue">
                            <span class="qw4" :class="`${item.index==1 ? 'qqw4' : ''}${item.index==2 ? 'qqqw4' : ''}${item.index==3 ? 'qqqqw4' : ''}`">{{ item.index }}</span>
                           <span class="qqw5"> {{ item.title}}</span>
                           <span class="qqw6">{{ item.hotValue }}</span>
                        </li>
                        <li v-show="index22 == 2" v-for="item  in data"   :key="item.index">
                            <span class="qw4" :class="`${item.index==1 ? 'qqw4' : ''}${item.index==2 ? 'qqqw4' : ''}${item.index==3 ? 'qqqqw4' : ''}`">{{ item.index }}</span>
                           <span class="qqw5"> {{ item.title}}</span>
                           <span class="qqw6">{{ item.hotValue }}</span>
                        </li>
                    </ul>
                </div>
            </div> 
    </div>
</template>

<script>
import { data } from '../../src/zhihu.js'
import { data1 } from '../weixin.js'
import { data2 } from '../baidutieba.js'
export default {
    name: 'HotsearchShequ',

    data() {
        return {
            data:data,
            data1:data1,
            data2:data2,
            index22:0,
            dingyue:[
                { 
                    id:1,
                    title:"微信阅读",
                    img:"https://files.codelife.cc/topsearch/mproPpoq6O.png",
                },
                 {
                    id:2,
                    title:"百度",
                    img:"https://files.codelife.cc/topsearch/mproPpoq6O.png",
                 },
                 {
                    id:3,
                    title:"知乎",
                    img:"https://files.codelife.cc/topsearch/mproPpoq6O.png",
                 },
            ],    
        };
    },

    mounted() {
        
    },

    methods: {
        dianji1(id){
            this.index22 = id
        }, 
    },
};
</script>

<style scoped>
.liqq:hover .qqw5{
   color: rgb(10, 174, 174);
}
.sousuo{
    width: 90%;
    height: 30px;
    background: rgb(240, 240, 240);
    border: none;
    padding-left: 20px;
    border-radius: 10px;
}
.qw4{
    float: left;
    width: 25px;
    height: 25px;
    color: black;
    background: rgb(201, 201, 201);
    line-height: 25px;
    border-radius: 5px;
    margin-left: 10px;
}
.qqw4{
    float: left;
    width: 25px;
    height: 25px;
    line-height: 25px;
    color: white;
    background: red;
    border-radius: 5px;
    margin-left: 10px;
}
.qqqw4{
    float: left;
    width: 25px;
    height: 25px;
    line-height: 25px;
    color: white;
    background: rgb(203, 97, 4);
    border-radius: 5px;
    margin-left: 10px;
}
.qqqqw4{
    float: left;
    width: 25px;
    height: 25px;
    line-height: 25px;
    color: white;
    background: rgb(203, 180, 4);
    border-radius: 5px;
    margin-left: 10px;
}
.qqw5{
    float: left;
    margin-left: 10px;
}
.qqw6{
    float: right;
    color: gray;
    margin-right: 10px;
}
.zong1{
    width: 100%;
    height: 80vh;
    /* background: red; */
}
.left{
    float: left;
    width: 25%;
    height: 100%;
    /* background: rebeccapurple; */
}
.right{
    float: right;
    width: 75%;
    height: 100%;
    color: black;
    /* background: rgb(66, 61, 71); */
}
li{
    list-style: none;
    /* background: rgb(66, 61, 71); */
    color: black;
    margin-top: 10px;
}
.valere{
    width: 99.3%;
    height: 98%;
    margin-top:10px;
    border: 3px solid rgb(241, 241, 241);
    border-left: none;
    border-bottom: none;
}
.valere li{
    width: 100%;
    height: 30px;
    line-height: 30px;
    display: block;
}
.qqw1{
    width: 30px;
    height:30px;
    float: left;
    border-radius: 10px;
    margin-left: 30px;
}
/* .qqw2{
    width: 30px;
    height: 30px;
    padding-left: 30px;
    float: left;
} */

.valere2{
    width: 100%;
    height: 98%;
    margin-top: 10px;
    border-top: 3px solid rgb(241, 241, 241);
    color: ghostwhite;
    overflow-y: scroll;
}
::-webkit-scrollbar{
      display: none;
}
.valere2 li{
    width: 100%;
    height: 30px;
}
.valere2 li:hover{
    color: rgb(85, 207, 241);
}
</style>