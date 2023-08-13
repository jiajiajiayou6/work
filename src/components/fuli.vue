<template>
    <div>
    <div id="fuli">
        <dl v-for="(item, index) in list  "  :key="index">
            <dd>
                <img class="img1" :src="item.img" alt="">
            </dd>
            <dt>
                <div class="left">
                    <p class="meiri"><b>{{ item.meiri }}</b></p>
                    <p class="tiaozhan">{{item.tiaozhan}}</p>
                </div>
                <div class="right">
                    <a href="#" class="wan">{{item.wanyiwan}}</a>
                </div>
            </dt>
        </dl>
    </div>
    </div>
</template>

<script>
export default {
    name: 'WorkFuli',

    data() {
        return {
            list:[
                {
                    id:1,
                    meiri:"每日一答",
                    tiaozhan:"挑战连续答对12道题",
                    wanyiwan:"玩一玩",
                    img:"https://img0.baidu.com/it/u=3021883569,1259262591&fm=253&app=120&size=w931&n=0&f=JPEG&fmt=auto?sec=1691514000&t=3b94efcd4cf30f38f638da5b2d67316a",
                },
                {
                    id:2,
                    meiri:"读书小队",
                    tiaozhan:"3人成对 共攒积分兑大奖",
                    wanyiwan:"立即组队",
                    img:"https://img1.baidu.com/it/u=3065838285,2676115581&fm=253&app=138&size=w931&n=0&f=JPEG&fmt=auto?sec=1691514000&t=c827a4cf757f4e15888ac7d36cee7be3",
                },
                {
                    id:3,
                    meiri:"周六组队抽体验卡",
                    tiaozhan:"挑战连续答对12道题",
                    wanyiwan:"立即组队",
                    img:"https://img2.baidu.com/it/u=1799171194,1010364318&fm=253&fmt=auto&app=120&f=JPEG?w=800&h=1501",
                },
                {
                    id:4,
                    meiri:"周四免费图书馆",
                    tiaozhan:"第316期 08:03-08.10",
                    wanyiwan:"立即查看",
                    img:"https://img2.baidu.com/it/u=483398814,2966849709&fm=253&fmt=auto&app=138&f=JPEG?w=889&h=500",
                },
                {
                    id:5,
                    meiri:"周二翻一翻",
                    tiaozhan:"第227期 08.01-08.08",
                    wanyiwan:"翻一番",
                    img:"https://img2.baidu.com/it/u=2312383180,3750420672&fm=253&fmt=auto&app=120&f=JPEG?w=1280&h=800",
                },
            ]
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style scoped>
a{
    text-decoration: none;
    color: rgb(140, 84, 0);
    font-size: 12px;
}
#fuli{
    width: 90%;
    position: relative;
    padding: 20px;
   height: 100%;
   background: rgb(238, 238, 238);
}
dl{
    width: 80%;
    height: 150px;
    background: rgb(255, 255, 255);
    position: relative;
    left: 0;
    right: 0;
    margin: auto;
    border-radius: 15px;
    margin-top: 10px;
    margin-bottom: 30px;
}
dd{
    width: 100%;
    height: 90px;
    border-radius: 15px 15px 0 0;
    
}
.img1{
    width: 100%;
    height: 90px;
    border-radius: 15px 15px 0 0;
}
.left{
    width: 70%;
    height: 60px;
    float: left;
}
.right{
    width: 30%;
    height: 60px;
    float: right;
}
.wan{
    width: 60px;
    height: 30px;
    background: rgb(234, 208, 170);
    display: inline-block;
    margin-top:15px;
    line-height: 30px;
    text-align: center;
    border-radius: 10px;
}
.meiri{
    margin-top: 8px;
    margin-left: 20px;
}
.tiaozhan{
    margin-left: 20px;
    font-size: 15px;
    color: gray;
}
</style>
