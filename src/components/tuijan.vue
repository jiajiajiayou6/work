<template>
    <div>
        <ul class="yl1">
            <li style="color: rgb(88, 143, 226);" v-for="(item, index) in list" :key="index" @click="dianji(item.id)">{{
                item.
                    name }}</li>
        </ul>
        <div class="yl2">
            <div class="qwe1" v-show="index == 1">
                <ul>
                    <li class="ul-li1" v-for="(item, index) in shuzu" :key="index">
                        <div style="float: left;">
                            <img class="all1" :src="item.img" alt="">
                        </div>
                        <div style="float: left;">
                            <p style="font-size: 20px;margin-left: 20px;"><b>{{ item.name }}</b></p>
                            <p style="font-size: 15px;margin-left: 20px;">{{ item.zuozhe }}|{{ item.zuozhe2 }}</p>
                            <p style="font-size: 15px;margin-left: 20px;">{{ item.ddu }}</p>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="qwe2" v-show="index == 2">
                <ul>
                    <li class="ul-li2" v-for="(item, index) in shuzu2" :key="index">
                        <div style="float: left;width: 70%;">
                            <p style="font-size: 20px;margin-left: 20px;margin-top: 5px;"><b>{{ item.name }}</b></p>
                            <p style="font-size: 15px;margin-left: 20px;color: gray;">{{ item.neirong1 }}</p>
                            <p style="font-size: 15px;margin-left: 20px;color: gray;">{{ item.neirong2 }}</p>
                            <p style="font-size: 15px;margin-left: 20px;color: gray;">{{ item.neirong3 }}</p>
                        </div>
                        <div style="float: left;width: 30%;">
                            <img class="all2" :src="item.img" alt="">
                        </div>
                    </li>
                </ul>
            </div>

            <div class="qwe3" v-show="index == 3">
                <ul>
                    <li class="ul-li1" v-for="(item, index) in shuzu" :key="index">
                        <div style="float: left;">
                            <img class="all1" :src="item.img" alt="">
                        </div>
                        <div style="float: left;">
                            <p style="font-size: 20px;margin-left: 20px;margin-top: 5px;"><b>{{ item.id }}.{{ item.name
                            }}</b></p>
                            <p style="font-size: 15px;margin-left: 20px;color: gray;padding-left: 15px;">{{ item.zuozhe }}
                            </p>
                        </div>
                    </li>
                </ul>
            </div>

            <div class="qwe4" v-show="index == 4">
                <ul>
                    <li class="ul-li4" v-for="(item, index) in shuzu" :key="index">
                        <div style="float: left;height: 80px;line-height: 80px;">{{ item.id }}</div>
                        <div style="float: left;margin-left: 10px;">
                            <img class="all1" :src="item.img" alt="">
                        </div>
                        <div style="float: left;">
                            <p style="font-size: 20px;margin-left: 20px;margin-top: 5px;"><b>{{ item.name }}</b></p>
                            <p style="font-size: 15px;margin-left: 20px;color: gray;">{{ item.zuozhe }}</p>
                            <p style="font-size: 15px;margin-left: 20px;color: gray;">{{ item.zuozhe2 }}</p>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
<!-- <component :is='currentView' keep-alive></component> -->
<script>

// import xiaoshuo from '../components/xiaoshuo.vue'
export default {
    name: 'WorkTuijan',
    data() {
        return {
            index: 1,
            list: [
                {
                    id: 1,
                    name: "推荐",
                    shuzu: "shuzu",
                },
                {
                    id: 2,
                    name: "分类"
                },
                {
                    id: 3,
                    name: "排行"
                },
                {
                    id: 4,
                    name: "文学艺术"
                },
            ],
            shuzu: [
                {
                    id: 1,
                    name: "红楼梦",
                    zuozhe: "曹雪芹著 无名氏徐续",
                    zuozhe2: "推荐值93.2%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/67/YueWen_36235932/t6_YueWen_36235932.jpg',
                    ddu: '大家都在读',
                },
                {
                    id: 2,
                    name: "孙子兵法与三十六计",
                    zuozhe: "张辉力",
                    zuozhe2: "推荐值82.6%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/98/cpPlatform_3300025251/t6_cpPlatform_3300025251.jpg',
                    ddu: '大家都在读',
                },
                {
                    id: 3,
                    name: "达芬奇密码",
                    zuozhe: "丹布朗",
                    zuozhe2: "推荐值82.7%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/9/cpplatform_ffxxfh9zishrhh1gdece8z/t6_cpplatform_ffxxfh9zishrhh1gdece8z1690196853.jpg',
                    ddu: '大家都在读',
                },
                {
                    id: 4,
                    name: "齐天大圣传",
                    zuozhe: "楚阳冬",
                    zuozhe2: "推荐值81.2%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/55/cpplatform_hfzlgvjurac4454cgfdkks/t6_cpplatform_hfzlgvjurac4454cgfdkks1690511343.jpg',
                    ddu: '大家都在读',
                },
                {
                    id: 5,
                    name: "骆驼祥子",
                    zuozhe: "老舍",
                    zuozhe2: "推荐值96.3%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/39/cpplatform_uavwwbmcljz28lruduqj72/t6_cpplatform_uavwwbmcljz28lruduqj721690363640.jpg',
                    ddu: '大家都在读',
                },
                {
                    id: 6,
                    name: "大医日出篇",
                    zuozhe: "马伯庸",
                    zuozhe2: "推荐值94.0%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/84/cpplatform_5w7t185qhfj9qfxdrrfytz/t6_cpplatform_5w7t185qhfj9qfxdrrfytz1689561935.jpg',
                    ddu: '大家都在读',
                },
                {
                    id: 7,
                    name: "最好的我们",
                    zuozhe: "八月长安",
                    zuozhe2: "推荐值92.7%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/55/cpplatform_2thuj2jlv1odkiylmdlcjr/t6_cpplatform_2thuj2jlv1odkiylmdlcjr1689825647.jpg',
                    ddu: '大家都在读',
                },
            ],
            shuzu2: [
                {
                    name: "精品小说",
                    neirong1: "1.长相思",
                    neirong2: "2.剑来",
                    neirong3: "3.三体",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/55/cpplatform_2thuj2jlv1odkiylmdlcjr/t6_cpplatform_2thuj2jlv1odkiylmdlcjr1689825647.jpg',
                },
                {
                    name: "历史",
                    neirong1: "1.明朝那些事儿",
                    neirong2: "2.长安的荔枝",
                    neirong3: "3.翦商：殷周之变与华夏新生",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/67/YueWen_36235932/t6_YueWen_36235932.jpg',
                },
                {
                    name: "文学",
                    neirong1: "1.我与地坛",
                    neirong2: "2.红楼梦",
                    neirong3: "3.平凡的时间",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/39/cpplatform_uavwwbmcljz28lruduqj72/t6_cpplatform_uavwwbmcljz28lruduqj721690363640.jpg',
                },
                {
                    name: "艺术",
                    neirong1: "1.生活蒙太奇",
                    neirong2: "2.故事：材质",
                    neirong3: "3.新摄影笔记",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/98/cpPlatform_3300025251/t6_cpPlatform_3300025251.jpg',
                },
                {
                    name: "人物传记",
                    neirong1: "1.邓小平时代",
                    neirong2: "2.毛泽东传",
                    neirong3: "3.苏东坡新传",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/84/cpplatform_5w7t185qhfj9qfxdrrfytz/t6_cpplatform_5w7t185qhfj9qfxdrrfytz1689561935.jpg',
                },
                {
                    name: "哲学宗教",
                    neirong1: "1.道德经",
                    neirong2: "2.次第花开",
                    neirong3: "3.图解易经",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/55/cpplatform_2thuj2jlv1odkiylmdlcjr/t6_cpplatform_2thuj2jlv1odkiylmdlcjr1689825647.jpg',
                },

            ],
        };



    },
    methods: {
        dianji(id) {
            this.index = id
            console.log(id);
        }
    },
};
</script>

<style scoped>
.yl1 {
    width: 95%;
    height: 50px;
    position: sticky;
    top: 130px;
    z-index: 1;
    background-color: rgb(255, 255, 255);
    display: flex;
}


li {
    list-style: none;

}

.yl1 li {
    /* float: left; */
    width: 25%;
    /* background-color: antiquewhite; */
    font-size: 18px;
    margin: auto;
    text-align: center;
}

li {
    list-style: none;
}

.ul-li1 {
    width: 100%;
    display: block;
    height: 80px;
    line-height: 25px;
    margin: auto;
    margin: 20px;
}

.all1 {
    width: 70px;
    height: 80px;
}

.yl2 {
    width: 90%;
    margin: auto;
}

.yl2 li {
    /* float: left; */
    width: 100%;
    /* background-color: antiquewhite; */
    font-size: 18px;
    margin: auto;
    margin-top: 20px;
    margin-bottom: 20px;
}

.ul-li2 {
    width: 100%;
    height: 105px;
    background-color: rgb(234, 234, 234);
    margin: 20px;
    line-height: 24px;
    /* padding-top: 10px; */
    border-radius: 15px;
}

.all2 {
    width: 90px;
    border-radius: 0 15px 15px 0;
    float: right;
    height: 105px;
}

.ul-li4 {
    width: 100%;
    height: 80px;
}
</style>