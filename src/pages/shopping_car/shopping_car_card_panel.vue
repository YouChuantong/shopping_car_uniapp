<!--
 * @Author: UpYou
 * @Date: 2021/1/8 11:52
 * @LastEditors: Please set LastEditors
 * @Description: 市场面板组件
 * 
-->

<template>
  <view class="shopping_car_card_panel">
    <view class="card_title">
      <check_box_selector />
      <text class="card_title_text">{{title}}</text>
    </view>
    <view class="shop_card">
      <view class="shop_card_name">
        <check_box_selector />
        <text class="shop_card_name_text">35号店铺</text>
      </view>
      <view class="commoditys">
        <view class="commodity">
          <check_box_selector />
          <view style="margin-left: 30rpx">
            <commodity-style></commodity-style>
          </view>
        </view>
      </view>
    </view>
    <view class="foot">
      <view class="foot_left">
        <text class="foot-text">配送费：</text>
        <text class="foot-text service_price">￥0</text>
      </view>
      <view class="foot_right">
        <text class="foot-text">小计：</text>
        <text class="foot-text amount_price">￥25</text>
      </view>
    </view>
  </view>
</template>

<script>
import commodityStyle from "./commodity_style";
import check_box_selector from "../../components/selector/check_box_selector"
export default {
    name: "shopping_car_card_panel",
  components: {
    commodityStyle,
    check_box_selector
  },
  props: {
      title: {
        type: String,
        default: "",
        required: true
      }
  }
}
</script>

<style scoped>
.card_title_text {
  font-size: 30rpx;
  font-weight: 600;
  margin-left: 30rpx;
}

.shopping_car_card_panel {
  border-radius: 20rpx;
  border: 1px solid #f7f7f7;
  background-color: #fff;
  box-shadow: 0 0 5rpx #f7f7f7;
}

.card_title,
.foot{
  height: 100rpx;
  border-bottom: 1px solid #f7f7f7;
  display: flex;
  align-items: center;
  padding: 0 30rpx;
}

.foot {
  border-bottom: none;
  border-top: 1px solid #f7f7f7;
  display: flex;
  flex-direction: row;
  margin-top: 30rpx;
  justify-content: space-between;
}

.shop_card {
  /*padding: 20rpx;*/
}

.shop_card_name_text {
  font-size: 28rpx;
  margin-left: 30rpx;
}

.shop_card_name {
  display: flex;
  align-items: center;
  height: 80rpx;
  flex-direction: row;
  padding-left: 30rpx;
}

.foot_left,
.foot_right{
  display: flex;
  flex-direction: row;
  align-items: center;
}

.foot-text {
  font-size: 25rpx;
}

.service_price,
.amount_price {
  font-size: 25rpx;
  color: #cf0016;
}

.commodity {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0 30rpx;
}
</style>