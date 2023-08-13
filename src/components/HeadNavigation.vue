<template>
  <div class="head">
    <ul>
      <li v-for="(item, index) in list" :key="index">
        <a href="#">{{ item.text }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "WorkspaceJsonHeadNavigation",
  components: {},
  data() {
    return {
      list: [
        {
          text: "我的订阅"
        },
        {
          text: "全部"
        },
        {
          text: "综合",
        },
        {
          text: "科技"
        },
        {
          text: "娱乐"
        },
        {
          text: "购物"
        }
      ],
      activeTab: 0
    };
  },

  mounted() {},

  methods: {}
};
</script>

<style scoped>
.head {
  width: 95%;
  height: 40px;
  margin: auto;
  border-bottom: 3px solid gray;
}
ul {
  width: 100%;
  height: 40px;
  line-height: 40px;
  display: flex;
  justify-content: space-around;
}
li a {
  font-size: 14px;
  color: #dfeaf3;
}
</style>