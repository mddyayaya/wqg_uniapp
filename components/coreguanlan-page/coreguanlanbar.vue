<template>
	<view class="guanlan_types_bar">
		<view class="guanlan_types_bar_items" :class="{seleted:seletcId == 1}">
			关注
		</view>
		<view class="guanlan_types_bar_items" :class="{seleted:seletcId == 2}">
			最新
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				seletcId:1
			}
		}
	}
</script>

<style lang="scss">
	.guanlan_types_bar{
		color: #FFFFFF;
		height: 60rpx;
		line-height: 60rpx;
		border-bottom: 1px solid #2B323B;
		display: flex;
		align-items: center;
		justify-content: center;
		&_items{
			margin-right: 58rpx;
			font-size: 24rpx;
			border-bottom: 2rpx solid rgba($color: #000000, $alpha: 0);
		}
		.seleted{
			border-bottom: 2rpx solid #02B9EE;
		}
	}
</style>
