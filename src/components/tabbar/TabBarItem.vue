<template>
  <div class="tab-bar-item" @click="clickbtn">
    <div v-if="!isClick">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-click"></slot>
    </div>
    <div :style="getColor">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  data() {
    return {
      // isClick: false
    };
  },
  props: {
    path: String,
    clickColor: {
      type: String,
      default: "#d81e06"
    }
  },
  computed: {
    isClick() {
      return this.$route.path.includes(this.path);
    },
    getColor() {
      return this.isClick ? { color: this.clickColor } : {};
    }
  },
  methods: {
    clickbtn() {
      this.$router.replace(this.path).catch(err => {});
    }
  }
};
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  height: 22px;
  margin-top: 4px;
  margin-bottom: 1px;
  vertical-align: middle;
}
</style>