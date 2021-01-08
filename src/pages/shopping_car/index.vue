<template>
	<view class="shopping_car">
		<view class="selected_count">
      <view class="selected_count_desc">
        <text class="selected_count_desc_text">当前已选1件商品(共2件)</text>
      </view>
      <view class="selected_count_edit">
        <text class="selected_count_edit_text">编辑</text>
      </view>
    </view>
    <view class="content">
      <view v-for="index in 10" :key="index"
        :style="{marginTop: index > 0 ? '30rpx' : 0}">
        <shopping-car-card-panel title="坡头市场"></shopping-car-card-panel>
      </view>
    </view>
    <view class="shop_desc">
      <view class="shop_desc_left">
        <check_box_selector/>
        <text class="select_all">全选</text>
      </view>
      <view class="shop_desc_right">
        <text class="foot-text">合计：</text>
        <text class="foot-text amount_price">￥25</text>
        <view class="submit">
          <text class="submit_text">结算</text>
        </view>
      </view>
    </view>
	</view>
</template>

<script>

import shoppingCarCardPanel from "./shopping_car_card_panel.vue"
import check_box_selector from "../../components/selector/check_box_selector"

	export default {
	  name: 'shopping_car',
    components: {
      shoppingCarCardPanel,
      check_box_selector
    },
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>
<style lang="css" scoped>
	.selected_count {
    background-color: #ffffff;
    width: 750rpx;
    padding: 0 30rpx;
    height: 90rpx;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    box-sizing: border-box;
    position: fixed;
    top: 0;
    left: 0;
    border-bottom: 1px solid #f8f8f8;
    align-items: center;
  }

  .selected_count_desc_text,
  .selected_count_edit_text{
    font-size: 30rpx;
    color: #939393;
  }

  .selected_count_edit_text {
    color: #cf0016;
  }

  .content {
    margin-top: 90rpx;
    padding: 30rpx;
    margin-bottom: 130rpx;
  }

  .shop_desc {
    height: 100rpx;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 0 30rpx;
    background-color: #fff;
    position: fixed;
    bottom: 0;
    left: 0;
    width: 750rpx;
    border-top: 1px solid #f8f8f8;
    align-items: center;
    box-sizing: border-box;
  }

  .select_all {
    font-size: 30rpx;
    color: #939393;
    margin-left: 30rpx;
  }

  .shop_desc_left,
  .shop_desc_right{
    display: flex;
    align-items: center;
  }

  .amount_price {
    font-size: 25rpx;
    color: #cf0016;
  }

  .foot-text {
    font-size: 28rpx;
  }

  .submit {
    width: 230rpx;
    height: 70rpx;
    background-color: #f09336;
    border-radius: 40rpx;
    margin-left: 30rpx;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .submit_text {
    font-size: 35rpx;
    color: #fff;
  }
</style>

<style>
page {
  background: #fcfcfc;
}
</style>