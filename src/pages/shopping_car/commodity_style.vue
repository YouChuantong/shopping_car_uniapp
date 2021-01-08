<!--
 * @Author: UpYou
 * @Date: 2021/1/8 12:10
 * @LastEditors: Please set LastEditors
 * @Description: 商品展示组件
 * 
-->

<template>
  <view class="commodity_style">
    <view class="left">
      <view class="cover">
        <image class="cover-image" src="/static/cover.jpeg"></image>
      </view>
      <view class="comm_desc">
        <text class="comm_name_text">五花肉</text>
        <view class="desc">
          <text class="desc_text">规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮规格：切块+加辣+不要猪皮</text>
        </view>
        <view class="price_amount">
          <view class="price">
            <text class="price_text">￥25.00</text>
          </view>
          <view class="amount">
            <counter num/>
          </view>
        </view>
      </view>
    </view>
    <view class="right"></view>
  </view>
</template>

<script>
import counter from "../../components/counter/counter"
export default {
    name: "commodity_style",
  components: {
    counter
  }
}
</script>

<style scoped>
.commodity_style {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.left {
  display: flex;
  flex-direction: row;
}

.cover {
  width: 140rpx;
  height: 140rpx;
  border-radius: 10rpx;
  overflow: hidden;
  margin-right: 20rpx;
  flex-shrink: 0;
}

.cover-image {
  width: 140rpx;
  height: 140rpx;
}

.comm_desc {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.comm_name_text {
  font-size: 28rpx;
  font-weight: 600;
}
.desc {
  flex-grow: 1;
}

.desc_text {
  font-size: 20rpx;
  color: #939393;
  display:-webkit-box;
  -webkit-box-orient:vertical;
  -webkit-line-clamp:2;
  overflow:hidden;
}

.price_amount {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: center;
}

.price_text {
  color: #cf0016;
  font-size: 28rpx;
}
</style>