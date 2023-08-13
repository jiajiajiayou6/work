<template>
  <div id="box">
    <div id="poa4">

      <div v-show="id == 1">
       <div class="dingbu">
          <b style="font-size: 30px;">微信读书</b>
        </div><!-- 顶部 -->
        <fuli></fuli>
        <shucheng></shucheng>
      </div>

      <div v-show="id == 2">
        <toubu></toubu><!-- 顶部 -->
        <yuedu></yuedu><!-- 阅读记录 -->
        <tuijan></tuijan><!-- 推荐导航 -->
        <!-- <xiaoshuo></xiaoshuo>小说 -->
      </div>

      <div v-show="id == 3">
        <toubu></toubu><!-- 顶部 -->
        <yuedu></yuedu><!-- 阅读记录 -->  
        <shucheng2></shucheng2><!-- 底部 -->
      </div>

    </div>

    <div id="poa5">
      <div id="buttom">
        <dl :style="{ color: activeindex == index ? 'rgb(88, 143, 226)' : '#000' }" v-for="(item, index) in list  " @click="dianji(index, item.id)" :key="index">
          <dd>
            <img style="width: 32px;height: 32px;margin-top:12px" :src="item.img" alt="">
          </dd>
          <dt>{{ item.name }}</dt>
        </dl>
      </div>
    </div>
  </div>
</template>
<script>
import toubu from './components/toubu.vue'
import yuedu from './components/yuedu.vue'
import tuijan from './components/tuijan.vue'
import fuli from './components/fuli.vue'
import shucheng from './components/shucheng1.vue'
import shucheng2 from './components/shucheng2.vue'
export default {
  data() {
    return {
      id: 2,
      activeindex: 1,
      color: '#000',
      list: [
        {
          id: 1,
          name: "福利",
          img: "https://img1.baidu.com/it/u=1524792439,419770891&fm=253&fmt=auto&app=138&f=JPEG?w=543&h=500",
        },
        {
          id: 2,
          name: "书城",
          img: "https://img0.baidu.com/it/u=3656623684,204076517&fm=253&fmt=auto&app=138&f=JPEG?w=610&h=314",
        },
        {
          id: 3,
          name: "听书",
          img: "https://img2.baidu.com/it/u=3791346349,2153430472&fm=253&fmt=auto&app=138&f=JPEG?w=494&h=500",
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
    }
  },
  methods: {
    dianji(index, id) {
      this.id = id
      this.activeindex = index
      // console.log(this.id);
      // console.log(this.activeindex);
      // if (this.index == index) {
      //     this.color = 'rgb(88, 143, 226)'
      // } else {
      //     this.color = '#000'
      // }
    }
  },
  components: {
    toubu,
    yuedu,
    tuijan,
    fuli,
    shucheng,
    shucheng2,
  },

}
</script>
<style scoped>
#box {
  width: 100%;
  height: 100vh;
  overflow-y: auto;
  overflow-x: hidden;
}
.dingbu{
  width: 100%;
  height: 80px;
  line-height: 80px;
  text-align: center;
  position: sticky;
  top: 0px;
  background-color: white;
  z-index: 1;
}

#poa4 {
  width: 100%;
}

#poa5 {
  width: 100%;
  height: 90px;
  z-index: 1;
  position: sticky;
  bottom: 0px;
}

#buttom {
  position: sticky;
  bottom: 0px;
  width: 100%;
  height: 90px;
  z-index: 1;
  color: rgb(106, 106, 106);
  background-color: rgb(255, 255, 255);
  display: flex;
  border-top: 1px solid black;
}

dl {
  width: 33%;
  height: 100%;
  margin: auto;
  text-align: center;
}

dd {
  width: 100%;
}

dt {
  font-size: 20px;
  margin-top: 10px;
}



li {
    list-style: none;

}
</style>
<style>
* {
  margin: 0;
  padding: 0;
}
html {
font-size: 16px;
}
@media screen and (max-width: 375px) {
html {
font-size: 14px;
}
}
@media screen and (max-width: 320px) {
html {
font-size: 12px;
}
}
</style>



