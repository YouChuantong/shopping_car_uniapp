<!--
 * @Author: UpYou
 * @Date: 2021/1/8 13:14
 * @LastEditors: Please set LastEditors
 * @Description: 计数器
 * 
-->

<template>
  <view class="counter">
    <view class="btn" @click="less">
      <text class="btn_text">-</text>
    </view>
    <text class="inp">{{num}}</text>
    <view @click="plus" class="btn" style="background-color: #f09336;">
      <text class="btn_text" style="color: #fff;">+</text>
    </view>
  </view>
</template>

<script>
export default {
  name: "counter",
  props: {
    abs: {
      type: Number,
      default: 0,
      required: false
    },
    max: {
      type: Number,
      required: false
    },
    min: {
      type: Number,
      required: false
    },
  },
  data() {
    return {
      num: 0
    }
  },
  methods: {
    plus() {
      if (this.max){
        if (this.num >= this.max){
          return;
        }
      }
      if (this.min) {
        if (this.num<this.min) {
          this.num = this.min;
        }
      } else {
        this.num = this.num + 1;
      }
      this.emitEv(this.num)
    },
    less() {
      if (this.min && this.num <= this.min) {
        this.num = 0;
        this.emitEv(this.num)
        return;
      }
      if (this.num > 0) {
        this.num = this.num - 1;
        this.emitEv(this.num)
      }
    },
    emitEv(val) {
      this.$emit("changed", val);
    }
  },
  watch: {
    num(val) {
      this.$emit("update:abs", val);
    },
    abs(val) {
      this.num = val;
    }
  }
}
</script>

<style scoped>
.counter {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.btn {
  width: 25rpx;
  height: 25rpx;
  border-radius: 50%;
  background-color: #fff;
  color: #f09336;
  border: 1px solid #f09336;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 23rpx;
}

.inp {
  padding: 0 20rpx;
  font-size: 28rpx;
}

.btn_text {
  text-align: center;
}
</style>