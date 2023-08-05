<template>
    <div class="yl2">
        <div>
            <ul>
                <li class="ul-li1" v-for="(item, index) in shuzu" :key="index">
                    <div style="float: left;">
                        <img class="all1" :src="item.img" alt="">
                    </div>
                    <div style="float: left;">
                        <p style="font-size: 20px;margin-left: 20px;"><b>{{ item.name }}</b></p>
                        <p style="font-size: 15px;margin-left: 20px;">{{ item.zuozhe }}</p>
                        <p style="font-size: 15px;margin-left: 20px;">{{ item.wocaole }}</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'WorkXiaoshuo',
    data() {
        return {
            shuzu: [
                {
                    name: "红楼梦",
                    zuozhe: "曹雪芹著 无名氏徐续 | 推荐值93.2%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/67/YueWen_36235932/t6_YueWen_36235932.jpg',
                    wocaole: '大家都在读',
                },
                {
                    name: "孙子兵法与三十六计",
                    zuozhe: "张辉力 | 推荐值82.6%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/98/cpPlatform_3300025251/t6_cpPlatform_3300025251.jpg',
                    wocaole: '大家都在读',
                },
                {
                    name: "达芬奇密码",
                    zuozhe: "丹布朗 | 推荐值82.7%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/9/cpplatform_ffxxfh9zishrhh1gdece8z/t6_cpplatform_ffxxfh9zishrhh1gdece8z1690196853.jpg',
                    wocaole: '大家都在读',
                },
                {
                    name: "齐天大圣传",
                    zuozhe: "楚阳冬 | 推荐值81.2%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/55/cpplatform_hfzlgvjurac4454cgfdkks/t6_cpplatform_hfzlgvjurac4454cgfdkks1690511343.jpg',
                    wocaole: '大家都在读',
                },
                {
                    name: "骆驼祥子",
                    zuozhe: "老舍 | 推荐值96.3%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/39/cpplatform_uavwwbmcljz28lruduqj72/t6_cpplatform_uavwwbmcljz28lruduqj721690363640.jpg',
                    wocaole: '大家都在读',
                },
                {
                    name: "大医日出篇",
                    zuozhe: "马伯庸 | 推荐值94.0%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/84/cpplatform_5w7t185qhfj9qfxdrrfytz/t6_cpplatform_5w7t185qhfj9qfxdrrfytz1689561935.jpg',
                    wocaole: '大家都在读',
                },
                {
                    name: "最好的我们",
                    zuozhe: "八月长安 | 推荐值92.7%",
                    img: 'https://weread-1258476243.file.myqcloud.com/weread/cover/55/cpplatform_2thuj2jlv1odkiylmdlcjr/t6_cpplatform_2thuj2jlv1odkiylmdlcjr1689825647.jpg',
                    wocaole: '大家都在读',
                },
            ]
        }
    }
};
</script>

<style scoped>
li {
    list-style: none;
}

.ul-li1 {
    width: 11rem;
    height: 3rem;
    line-height: 1rem;
    margin: auto;
    margin: 20px;
}

.all1 {
    width: 2rem;
    height: 3rem;
}
</style>