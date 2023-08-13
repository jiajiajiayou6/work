<template>
    <div>
        <div id="content1" v-show="id == 1">
        </div>
        <div id="content2" v-show="id == 2">
        </div>
        <div id="content3" v-show="id == 3">
        </div>
        <div id="content4" v-show="id == 4">
        </div>
        <div id="content5" v-show="id == 5">
        </div>
        <div id="content4" v-show="id == 6">
        </div>
        <div id="content5" v-show="id == 7">
        </div>
    </div>
</template>

<script>
export default {
    name: 'HotsearchXuanzeye',

    data() {
        return {
            id: 1,
            activeindex: 0,
            dingyue:[
                {
                    id:1,
                    title:"微信阅读",
                    img:"https://files.codelife.cc/topsearch/mproPpoq6O.png",
                    con:[
                    {
                        id:1,
                        name:"三体（全集）",
                        tuijianren:"刘慈欣",
                        tuijianzhi:"推荐值",
                        img2:"",
                    },
                    {
                        id:2,
                        name:"长安的荔枝",
                        tuijianren:"马伯庸",
                        tuijianzhi:"推荐值",
                        img2:"",
                    },
                    {
                        id:3,
                        name:"明朝那些事",
                        tuijianren:"当年明月",
                        tuijianzhi:"推荐值",
                        img2:"",
                    },
                    {
                        id:4,
                        name:"活着",
                        tuijianren:"余华",
                        tuijianzhi:"推荐值",
                        img2:"",
                    },
                    {
                        id:5,
                        name:"平凡的世界",
                        tuijianren:"路遥",
                        tuijianzhi:"推荐值",
                        img2:"",
                    },
                    {
                        id:6,
                        name:"追风筝的人",
                        tuijianren:"卡勒德 胡塞尼",
                        tuijianzhi:"推荐值",
                        img2:"",
                    },
                    {
                        id:7,
                        name:"杀死一只知更鸟",
                        tuijianren:"哈珀 李",
                        tuijianzhi:"推荐值",
                        img2:"",
                    },
                    ],
                 },
                 {
                    id:2,
                    title:"百度",
                    img:"",
                    con:{
                        id:1,
                        name:"三体（全集）",
                        tuijianren:"刘慈欣",
                        tuijianzhi:"推荐值",
                        img2:"",
                    } 
                 },
                 {
                    id:3,
                    title:"知乎",
                    img:"",
                    con:{
                        id:1,
                        name:"三体（全集）",
                        tuijianren:"刘慈欣",
                        tuijianzhi:"推荐值",
                        img2:"",
                    } 
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

</style>