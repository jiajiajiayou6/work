<template>
    <div class="qwe1">
        <h2 class="h3">影视热门榜</h2>
        <ul>
            <li class="ul-li1"  v-for="(  item, index  ) in   shuzu" :key="index">
                <div style="float: left;">
                    <img class="all1" :src="item.img" alt="">
                </div>
                <div style="float: left;">
                    <p style="font-size: 20px;margin-left: 20px;"><b>{{ item.name }}</b></p>
                    <p style="font-size: 15px;margin-left: 20px;">{{ item.zuozhe }}</p>
                    <p style="font-size: 15px;margin-left: 20px;">{{ item.ddu }}</p>
                </div>
            </li>
        </ul>
        <div class="chakan1"><a href="#">查看更多</a></div>
    </div>
</template>
<script>
export default {
    name: 'WorkShucheng2',
    data() {
        return {
            shuzu: [
                {
                    id: 1,
                    name: "庆余年",
                    zuozhe: "猫腻 | 讲书人：阅文听书",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/67/YueWen_36235932/t6_YueWen_36235932.jpg',
                    ddu: '362人今日在听',
                },
                {
                    id: 2,
                    name: "鬼吹灯(盗墓者的经历)",
                    zuozhe: "本物天下霸唱|讲书人：道听途说",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/98/cpPlatform_3300025251/t6_cpPlatform_3300025251.jpg',
                    ddu: '132人今日在听',
                },
                {
                    id: 3,
                    name: "雪中悍刀行",
                    zuozhe: "烽火戏诸侯|讲书人：企鹅有声",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/9/cpplatform_ffxxfh9zishrhh1gdece8z/t6_cpplatform_ffxxfh9zishrhh1gdece8z1690196853.jpg',
                    ddu: '104人今日在听',
                },
            ],
        };
    },
    mounted() {
    },
    methods: {
    },
};
</script>
<style scoped>
.qwe1{
  width: 100%;
  height: 400px;
}
.all1 {
    width: 70px;
    height: 80px;
}
.h3{
    margin-left: 20px;
}
a{
    text-decoration: none;
    color: black;
    width: 100%;
    height: 80px;
    line-height: 80px;
    background: aqua;
}
.chakan1{
    width: 100%;
    height: 80px;
    line-height: 80px;
    text-align: center;
}
.ul-li1 {
    width: 100%;
    display: block;
    height: 80px;
    line-height: 25px;
    margin: auto;
    margin: 20px;
}
</style>