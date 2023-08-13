<template>
    <div id="top-buttom">
        <div id="top-buttom-top">
            <img class="w1"
                src="https://img1.baidu.com/it/u=3129770633,3933811923&fm=253&fmt=auto&app=138&f=JPEG?w=889&h=500" alt="">
            <span class="w2">三七二十一</span>
            <span class="w3">体验卡今日到期</span>
            <a class="w4" href="./shezhi.vue">设置</a>

        </div>
        <div id="top-buttom-buttom">
            <div id="t1">
                <img class="w5"
                    src="https://weread-1258476243.file.myqcloud.com/weread/cover/25/cpplatform_8numzl8erzinxvfsk3p9jv/t6_cpplatform_8numzl8erzinxvfsk3p9jv1685508354.jpg"
                    alt="">
            </div>
            <span class="shujia">书架</span>
            <svg t="1691251155208" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
                p-id="2284" width="16" height="16">
                <path d="M369.5 980.9l-81.8-73.6 354.4-393.8-375-394.7L346.9 43l445 468.5z" p-id="2285" fill="#8a8a8a">
                </path>
            </svg>
        </div>
    </div>
</template>

<script>
export default {
    name: 'WorkYuedu',
};
</script>

<style scoped>
a {
    text-decoration: none;
    color: gray;
}

#top-buttom {
    width: 91.5%;
    margin: auto;
    margin-top: 140px;
    height: 150px;
    background-color: #585a61;
    border-radius: 15px;
    margin-bottom: 10px;
}

#top-buttom-top {
    width: 100%;
    height: 45px;
    line-height: 45px;
    border-radius: 10px 10px 0 0;
    /* background-color: rgb(156, 35, 35); */
}

#top-buttom-buttom {
    width: 100%;
    height: 105px;
    /* background-color: beige; */
    border-radius: 0 0 10px 10px;
}

.w1 {
    width: 40px;
    height: 40px;
    /* background-color: aqua; */
    float: left;
    margin-left: 10px;
    margin-top: 3px;
    border-radius: 20px;
}

.w2 {
    float: left;
    font-size: 15px;
    margin-left: 10px;
    color: white;
}

.w3 {
    float: left;
    color: rgb(203, 202, 202);
    font-size: 15px;
    margin-left: 10px;
}

.w4 {
    float: right;
    color: white;
    text-align: center;
    width: 50px;
    height: 35px;
    font-size: 15px;
    line-height: 35px;
    margin-top: 7px;
    border-radius: 20px 0 0 20px;
    background-color: rgb(163, 163, 163);
}

#t1 {
    margin-top: 10px;
    width: 65px;
    height: 85px;
    float: left;
    margin-left: 10px;
    /* background-color: aqua; */
}

.w5 {
    width: 65px;
    height: 85px;
}

.shujia {
    float: right;
    width: 15px;
    height: 40px;
    display: block;
    font-size: 15px;
    position: relative;
    top: 28px;
    left: -25px;

}

#top-buttom-buttom svg {
    float: right;
    position: relative;
    top: 38px;
    left: 10px;

}
</style>