<template>
    <div>
        <div class="zong1">
                <div class="left">
                    <ul class="valere">
                        <li><input class="sousuo" type="text" name="" placeholder="搜索" id=""></li>
                        <li class="liqq" :style="{ background: index22 == index ? 'rgb(88, 143, 226)' : '' }"  v-for="(item, index) in dingyue"  :key="item" @click="dianji1(index, item.id)"> 
                            <svg class="qqw2" data-v-d7b5176e="" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 24 24"><path d="M11 18c0 1.1-.9 2-2 2s-2-.9-2-2s.9-2 2-2s2 .9 2 2zm-2-8c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2zm0-6c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2zm6 4c1.1 0 2-.9 2-2s-.9-2-2-2s-2 .9-2 2s.9 2 2 2zm0 2c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2zm0 6c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2z" fill="currentColor"></path></svg>
                            <img class="qqw1" :src="item.img">
                            <span class="qqw5">{{ item.title }}</span>
                            <svg class="qqw3" data-v-d7b5176e="" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1024 1024"><path fill="currentColor" d="M176 416a112 112 0 1 1 0 224 112 112 0 0 1 0-224zm336 0a112 112 0 1 1 0 224 112 112 0 0 1 0-224zm336 0a112 112 0 1 1 0 224 112 112 0 0 1 0-224z"></path></svg>
                            <button class="shanchu" @click="shanchu(item)">删除</button>
                        </li>
                    </ul>
                </div>
                <div class="right">
                    <ul class="valere2">
                        <li v-show="index22 == 0" v-for="item  in data1"  :key="item.index">
                            <span class="qw4" :class="`${item.index==1 ? 'qqw4' : ''}${item.index==2 ? 'qqqw4' : ''}${item.index==3 ? 'qqqqw4' : ''}`">{{ item.index }}</span>
                           <span class="qqw5"> {{ item.title}}</span>
                           <span class="qqw6">{{ item.hotValue }}</span>
                        </li>
                          <li v-show="index22 == 1" v-for="item  in data2"  :key="item.title">
                            <span class="qw4" :class="`${item.index==1 ? 'qqw4' : ''}${item.index==2 ? 'qqqw4' : ''}${item.index==3 ? 'qqqqw4' : ''}`">{{ item.index }}</span>
                           <span class="qqw5"> {{ item.title}}</span>
                           <span class="qqw6">{{ item.hotValue }}</span>
                        </li>
                        <li v-show="index22 == 2" v-for="item  in data"  :key="item.hotValue">
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
    name: 'HotsearchWodedingyue',

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
        shanchu(item){
            console.log(item);
            this.dingyue.splice(this.dingyue.indexOf(item),1)
            // if(this.dingyue.id==0){
            //     console.log(1);
            //     return
            // }else if(this.id==1){
            //     console.log(2);
            //     return
            // }else if(this.id==2){
            //     console.log(3);
            //     return
            // }else{
            //     return
            // }
        },
        dianji1(id){
            this.index22 = id
        },
    },
};
</script>

<style scoped>
.shanchu{
    padding: 2px 5px;
    background: rgb(245, 245, 245);
    border-radius: 5px;
    float: right;
    margin-right: 10px;
    margin-top: 3px;
    display: none;
    border: 1px solid gray;
}
.liqq:hover .shanchu{
    display: inline; 
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
    line-height: 25px;
    background: rgb(201, 201, 201);
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
.liqq:hover .qqw5{
    color: rgb(48, 160, 197);
}
.qqw6{
    float: right;
    color: gray;
    margin-right: 10px;
}
.zong1{
    width: 100%;
    height: 80vh;
    /* background: rgb(177, 177, 177); */
    
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
    /* background: rgb(66, 61, 71);1x */
}
li{
    list-style: none;
    margin-top: 10px;
}
.valere{
    width: 99.3%;
    height: 98%;
    margin-top:10px;
    border: 3px solid rgb(209, 209, 209);
    border-left: none;
    border-bottom: none;
}
.valere li{
    width: 100%;
    height:30px;
    line-height: 30px;
    display: block;
}
.qqw1{
    width: 30px;
    height:30px;
    float: left;
    border-radius: 10px;
}
.qqw2{
    width: 30px;
    height: 30px;
    float: left;
}
.qqw3{
    width: 30px;
    height: 30px;
    float: right;
}
.valere2{
    width: 100%;
    height: 98%;
    margin-top: 10px;
    border-top: 3px solid rgb(209, 209, 209);
    color: rgb(0, 0, 0);
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