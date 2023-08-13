<template>
  <div class="leftdata">
    <ul>
      <li>
        <input type="text" placeholder="搜索" />
      </li>
      <li v-for="(item, index) in str" :key="index">
        <a href="#">
          <svg
            data-v-d7b5176e
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            viewBox="0 0 24 24"
            id="listers"
          >
            <path
              d="M11 18c0 1.1-.9 2-2 2s-2-.9-2-2s.9-2 2-2s2 .9 2 2zm-2-8c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2zm0-6c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2zm6 4c1.1 0 2-.9 2-2s-.9-2-2-2s-2 .9-2 2s.9 2 2 2zm0 2c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2zm0 6c-1.1 0-2 .9-2 2s.9 2 2 2s2-.9 2-2s-.9-2-2-2z"
              fill="currentColor"
            />
          </svg>
          <img :src="item.imgse" alt width="20px" height="20px" />
          <span>{{ item.name }}</span>
          <b>...</b>
        </a>
      </li>
    </ul>
    <img src alt />
  </div>
</template>

<script>
export default {
  name: "WorkspaceJsonLeftNavigation",

  data() {
    return {
      str: [
        {
          imgse: "https://files.codelife.cc/topsearch/Jb0vmloB1G.png",
          name: "百度"
        },
        {
          imgse: "https://files.codelife.cc/topsearch/KqndgxeLl9.png",
          name: "微博"
        },
        {
          imgse: "https://files.codelife.cc/topsearch/mproPpoq6O.png",
          name: "知乎"
        }
      ]
    };
  },

  mounted() {},

  methods: {}
};
</script>

<style  scoped>
.leftdata {
  float: left;
  margin-top: 10px;
  width: 24%;
  height: 512px;
  border-top: 1px solid gray;
  border-right: 1px solid gray;
}
ul {
  width: 100%;
  height: 100%;
}
li {
  width: 100%;
  height: 30px;
  line-height: 25px;
}
li input {
  position: relative;
  left: 5px;
  width: 90%;
  height: 25px;
  border: none;

  border-radius: 10px;
  padding-left: 10px;
  background-color: #2a2a2c;
}
li a {
  position: relative;
  left: 10px;
  display: block;
  width: 80%;
  height: 30px;
}
li img {
  position: relative;
  top: 5px;
  border-radius: 5px;
}
li span {
  position: relative;
  left: 5px;
  font-size: 15px !important;
  color: #fff;
}
li b {
  position: relative;
  top: -3px;
  left: 8px;
  float: right;
  color: #fff;
}
#listers {
  position: relative;
  top: 5px;
  width: 20px;
  height: 20px;
  color: #fff;
}
li span:hover {
  color: blue;
}
li b:hover {
  color: blue;
}
</style>