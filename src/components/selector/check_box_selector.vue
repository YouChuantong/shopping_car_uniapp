<!--
 * @Author: UpYou
 * @Date: 2021/1/8 12:45
 * @LastEditors: Please set LastEditors
 * @Description: 选择框 - 圆
 * 
-->

<template>
  <view class="check_box_selector" :class="{back: state}" @click="change">
    <image v-if="state" class="selected" src="/static/selector_img/xuanze.png"></image>
  </view>
</template>

<script>
export default {
  name: "check_box_selector",
  props: {
    selected: {
      type: Boolean,
      default: false,
      required: false
    }
  },
  data() {
    return {
      state: false
    }
  },
  watch: {
    selected(val) {
      this.state = val
    }
  },
  methods: {
    change() {
      this.state = !this.state;
      this.$emit("changed", this.state);
    }
  }
}
</script>

<style scoped>
.check_box_selector {
  height: 40rpx;
  width: 40rpx;
  border-radius: 50%;
  border: 1px solid #dcdcdc;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #fff;
  transition: all .1s;
}

.back {
  background-color: #f09336;
  border: 1px solid #f09336;
}

.selected {
  height: 30rpx;
  width: 30rpx;
  opacity: 1;
  transition: all .1s;
}

</style>