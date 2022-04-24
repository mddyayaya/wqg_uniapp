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
		background-color: #fff;
		padding: 20rpx;
		box-sizing: border-box;
		&_item{
			margin-top: 28rpx;
			width: 100%;
			height: 240rpx;
			display: flex;
			justify-content: space-between;
			.item_image{
				overflow: hidden;
				width: 340rpx;
				height: 100%;
				border-radius: 20rpx;
				margin-right: 20rpx;
			}
			.item_text_wrap{
				flex: 1;
				font-size: 24rpx;
				color: #333333;
				.item_title{
					font-weight: bold;
					color: #000;
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
