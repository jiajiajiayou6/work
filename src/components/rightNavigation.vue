<template>
  <div class="rightdata">
    <ul>
      <li class="li1">
        <img
          src="https://files.codelife.cc/topsearch/Jb0vmloB1G.png"
          alt
          width="25px"
          height="25px"
        />
        <span>百度.实时热点</span>
      </li>
      <li v-for="(item, index) in str" :key="index">
        <span></span>
        {{ item.title }}
      </li>
    </ul>
  </div>
</template>

<script>
import rightdata from "../components/rightdata.json";
export default {
  name: "WorkspaceJsonRightNavigation",

  data() {
    return {
      str: []
    };
  },

  mounted() {
    console.log(rightdata);
    this.str = rightdata;
  },

  methods: {}
};
</script>

<style scoped>
.rightdata {
  margin-top: -13.8px;
  float: right;
  width: 75.87%;
  height: 512px;
  border-top: 1px solid gray;
}
ul {
  width: 90%;
  height: 100%;
  margin: auto;
}
.li1 {
  width: 100%;
  height: 40px;
  border-bottom: 1px solid gray;
}
.li1 img {
  position: relative;
  top: 7px;
  border-radius: 50%;
}
.li1 span {
  position: relative;
  left: 5px;
  color: #fff;
}
</style>