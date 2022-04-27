<template>
	<view class="area-wrap">
		<view class="title">
			<view>场地</view>
			<view class="zicheng"></view>
		</view>
		<view class="area-swipers">
			<!-- <u-swiper >
			</u-swiper> -->
			<view class="area-swipers-top">
				<image :src="nearbySlider[0].imageUrl" mode=""></image>
			</view>
			<view class="area-swipers-center">
				<image src="../../static/images/common/main_logo.png" mode=""></image>
			</view>
			<view class="area-swipers-center1">
				{{nearbyStoreListData[0].storeName}}
			</view>
			<view class="area-swipers-center_line">
				<image src="../../static/images/common/main_line.png" mode="widthFix"></image>
			</view>
			<view class="area-swipers-center_images">
				<view class="images_item" >
					<view class="gou">
						<image src="../../static/images/common/main_icon1.png" mode=""></image>
					</view>
					<view class="images">
						<u-lazy-load class="item_image" :image="item.thumbnail"></u-lazy-load>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	let that;
	export default{
		data(){
			return{
				list: [{
					image: 'https://cdn.uviewui.com/uview/swiper/1.jpg',
					title: '昨夜星辰昨夜风，画楼西畔桂堂东'
				},
				{
					image: 'https://cdn.uviewui.com/uview/swiper/2.jpg',
					title: '身无彩凤双飞翼，心有灵犀一点通'
				},
				{
					image: 'https://cdn.uviewui.com/uview/swiper/3.jpg',
					title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
				}
			],
			}
		},
		props:{
			nearbySlider:{
                default: function () {
                    return []
                },
			},
			nearbyData1:{
                default: function () {
                    return []
                },
			},
			nearbyData2:{
                default: function () {
                    return []
                },
			},
			nearbyData3:{
                default: function () {
                    return []
                },
			}
		},
		created() {
			that = this;
			that.getCurrentLocation();
		},
		methods:{
			// 获取当前经纬度
			getCurrentLocation(){
				that.$emit("nearbyStoreList","TplSlider")
				that.$emit("nearbyStoreList","TplIndexBanner1")
				that.$emit("nearbyStoreList","TplIndexBanner2")
				that.$emit("nearbyStoreList","TplIndexBanner3")
			}
		}
	}
</script>

<style lang="scss">
	.area-wrap{
		box-sizing: border-box;
		padding: 0 26rpx;
		.title{
			display: flex;
			align-items: center;
			width: 146rpx;
			line-height: 60rpx;
			height: 60rpx;
			display: block;
			text-align: center;
			color: #fff;
			font-size: 28rpx;
			background: url(../../static/images/indexMenus/titleBg.png) no-repeat;
			background-size: 100% 100%;
		}
		.zicheng{
			flex: 1;
		}
		.area-swipers{
			margin-top: 15rpx;
			width: 100%;
			background-color: #000;
			border-radius: 10rpx;
			padding-bottom: 20rpx;
			overflow: hidden;
			.area-swipers-top{
				width: 100%;
				height: 219rpx;
				background-color: #ededed;
				image{
					width: 100%;
					height: 100%;
				}
			}
			.area-swipers-center{
				width: 112rpx;
				height: 112rpx;
				margin:-56rpx auto 0 auto;
				image{
					width: 100%;
					height: 100%;
				}
			}
			.area-swipers-center1{
				width: 180rpx;
				margin:7rpx auto 0 auto;
				text-align: center;
				font-size: 32rpx;
				font-weight: bold;
				color: #fff;
				letter-spacing: 3rpx;
			}
			.area-swipers-center_line{
				width: 100%;
				margin-top: -20rpx;
				image{
					width: 100%;
				}
			}
			.area-swipers-center_images{
				padding: 0 18rpx;
				display: flex;
				align-items: center;
				justify-content: space-between;
				.images_item{
					position: relative;
					width: 210rpx;
					height: 160rpx;
					background-color: #333;
					.gou{
						position: absolute;
						height: 72rpx;
						width: 29rpx;
						image{
							width: 100%;
							height: 100%;
						}
					}
					.images{
						position: absolute;
						width: 100%;
						height: 100%;
						left: 0;
						top: 0;
						
					}
				}
				.images_item:last-child{
					transform: rotate(-10deg) translateY(-10rpx);
					.gou{
						top: -20rpx;
						right: 10rpx;
						transform: rotate(10deg)
					}
				}
				.images_item:nth-child(1){
					transform: rotate(10deg) translateY(-10rpx);
					.gou{
						top: -20rpx;
						left: 10rpx;
						transform: rotate(10deg)
					}
				}
				.images_item:nth-child(2){
					transform: scale(0.95);
					.gou{
						top: -20rpx;
						left: 50%;
						transform: translateX(-50%);
					}
				}
			}
		}
	}
</style>
