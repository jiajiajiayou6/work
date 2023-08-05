<template>
    <div id="top">
        <b>微信读书</b><br>
        <svg t="1691066671752" class="icon1" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
            p-id="2294" width="16" height="16">
            <path
                d="M384 128c140.8 0 256 115.2 256 256S524.8 640 384 640 128 524.8 128 384s115.2-256 256-256m0-64C207.2 64 64 207.2 64 384s143.2 320 320 320 320-143.2 320-320S560.8 64 384 64z m294.4 569.6l-45.6 45.6 272 272 45.6-45.6-272-272z"
                p-id="2295" fill="#8a8a8a"></path>
        </svg>
        <input type="text" name="text" id="text" placeholder="搜索">
    </div>
</template>

<script>
export default {
    name: 'WorkToubu',
};
</script>

<style scoped>
#top {
    width: 100%;
    height: 130px;
    /* top: 20px; */
    position: fixed;
    z-index: 1;
    text-align: center;
    background-color: rgb(255, 255, 255);
}

b {

    font-size: 30px;
    position: relative;
    top: 10px;
}

#text {
    position: relative;
    top: 15px;
    left: -8px;
    background-color: rgb(238, 238, 238);
    width: 75%;
    padding-left: 40px;
    height: 40px;
    border-radius: 45px;
    border: none;

}

.icon1 {
    position: relative;
    left: 25px;
    top: 20px;
    /* top: 5px; */
    z-index: 1;
}
</style>