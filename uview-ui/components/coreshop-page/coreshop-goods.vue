<template>
    <view class="goods_list">
       <view class="goods_list_item" v-for="item in 6" @click="goSigin">
			<u-lazy-load class="item_image" :image="item.src"></u-lazy-load>
			<view class="item_text_wrap">
				<view class="item_title u-line-2">
					文沁阁---图书参观活动文沁阁图书参观活动文沁阁图书参观活动文沁阁图书参观活动文沁阁
				</view>
				<view class="item_time">
					2022-11-25至2021-12-30 10:00-17:00
				</view>
				<view class="item_address">
					地点：北京东城区
				</view>
				<view class="item_price">
					¥68起
				</view>
				<view class="item_bottom_bar">
					<view class="item_has_nohss"></view>
					<view class="item_haseen">
						4596人看过
					</view>
				</view>
			</view>
       </view>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                current: 0,
            };
        },
        filters: {
        },
        name: "coreshopgoods",
        props: {
        },
        computed: {
        },
        methods: {
			goSigin(){
				// 去报名
				let url = '/pages/sigin/sigin'
				this.$u.route(url)
			}
        },
    }
</script>

<style scoped lang="scss">
	.goods_list{
		width: 100%;
		padding: 23rpx;
		box-sizing: border-box;
		&_item{
			margin: 0 20rpx 31rpx 20rpx;
			height: 199rpx;
			background-color: #2B323B;
			transform: skew(-20deg);
			box-shadow: 7rpx 8rpx 19rpx 2rpx rgba(0, 0, 0, 0.19);
			border-radius: 10rpx;
			display: flex;
			justify-content: space-between;
			.item_image{
				transform: skew(40deg);
				overflow: hidden;
				width: 271.2rpx;
				height: 100%;
				border-radius: 20rpx;
				margin-right: 16rpx;
			}
			.item_text_wrap{
				flex: 1;
				font-size: 24rpx;
				color: #fff;
				.item_title{
					font-weight: bold;
					font-weight: bold;
				}
				.item_time{
					margin-top: 5rpx;
				}
				.item_bottom_bar{
					display: flex;
					justify-content: space-between;
					align-items: center;
				}
			}
		}
	}
</style>
