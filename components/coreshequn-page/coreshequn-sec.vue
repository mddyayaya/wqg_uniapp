<template>
	<view class="coreshequnMygroup">
		<view class="group_title">
			<view class="titleBg mySec">
				我的秘密空间
			</view>
		</view>
		<view class="mySec_list">
			<view class="mySec_list_item" v-for="(item,index) in 6">
				<view class="mySec_list_item_top">
					<view class="info_wrap">
						<view class="avater">
							<u-lazy-load 
							:image="require('@/static/images/common/test_pic.png')"></u-lazy-load>
						</view>
						<view class="infos">
							<view class="infos_name">
								刘畊宏
							</view>
							<view class="infos_time">
								一小时前 · 北京
							</view>
						</view>
					</view>
					<view class="open_close">
						<view class="open_close_icon" v-if="index == 0">
							<u-icon :name="require('@/static/images/common/open.png')" size="25"></u-icon>
							<text>对外公开</text>
						</view>
						<view class="open_close_icon" v-else>
							<u-icon :name="require('@/static/images/common/close.png')" size="25"></u-icon>
							<text>取消公开</text>
						</view>
					</view>
				</view>
				<view class="mySec_list_item_cont">
					<view class="item_text">
						人如果没有了希望和梦想，那么跟咸鱼有什么区别？人如果心里除了工作还是工作，那人生还有什么意义？
					</view>
					<view class="item_images" v-if="index > 3">
						<view class="box-1" v-for="items in 9">
							<!-- <u-lazy-load
							:image="require('@/static/images/common/test_pic.png')"></u-lazy-load> -->
						</view>
					</view>
				</view>
				<view class="save_diss_wrap">
					<view class="save_diss">
						<view class="">
							<u-icon :name="require('@/static/images/common/heart.png')" size="35"></u-icon>
							<text>24</text>
						</view>
						<view class="">
							<u-icon :name="require('@/static/images/common/diss.png')" size="35"></u-icon>
							<text>50</text>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data(){
			return{
				arr:6
			}
		},
		methods:{
		}
	}
</script>

<style lang="scss">
	.mySec{
		width: 194rpx !important;
		margin: 40rpx 0 30rpx 0;
	}
	.mySec_list{
		width: 100%;
		padding-bottom: 20rpx;
		.mySec_list_item{
			padding: 30rpx 0;
			border-bottom: 2rpx solid #61676F;
			&_top{
				display: flex;
				justify-content: space-between;
				align-items: center;
				.info_wrap{
					flex: 1;
					display: flex;
					align-items: center;
					.avater{
						height: 90rpx;
						width: 90rpx;
						overflow: hidden;
						border-radius: 50%;
						background: #ededed;
						overflow: hidden;
						margin-right: 14rpx;
					}
					.infos{
						color: #fff;
						.infos_name{
							font-size: 27rpx;
						}
						.infos_time{
							font-size: 24rpx;
							margin-top: 16rpx;
						}
					}
				}
				.open_close{
					width: 120rpx;
					color: #02B9EE;
					font-size: 18rpx;
					display: flex;
					align-items: center;
					margin-left: 5rpx;
					.open_close_icon{
						display: flex;
						align-items: center;
						align-content: flex-start;
						text{
							margin-left: 7rpx;
						}
					}
				}
			}
			&_cont{
				.item_text{
					color: #fff;
					font-size: 24rpx;
					margin: 25rpx 0;
					line-height: 40rpx;
				}
				.item_images{
					display: flex;
					flex-wrap: wrap;
					width: 100%;
					overflow: hidden;
					.box-1{
						width:217rpx;
						height: 217rpx;
						margin-right: 20rpx;
						margin-bottom: 20rpx;
						border-radius: 20rpx;
						background-color: #ededed;
					}
					.box-1:nth-child(3n){
						margin-right: 0;
					}
				}
			}
			.save_diss_wrap{
				display: flex;
				justify-content: flex-end;
				align-items: center;
				margin-top: 30rpx;
				.save_diss{
					display: flex;
					align-items: center;
					font-size: 26rpx;
					color: #fff;
					view{
						margin-left: 20rpx;
						display: flex;
						align-items: center;
						text{
							margin-left: 13rpx;
						}
					}
				}
			}
		}
	}
</style>
