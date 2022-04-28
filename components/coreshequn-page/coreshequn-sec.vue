<template>
	<view class="coreshequnMygroup">
		<view class="group_title">
			<view class="titleBg mySec">
				我的秘密空间
			</view>
		</view>
		<view class="mySec_list">
			<view class="mySec_list_item" v-for="(item,index) in 2">
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
							<u-icon :name="require('@/static/images/common/open.png')"></u-icon>
							<text>对外公开</text>
						</view>
						<view class="open_close_icon" v-else>
							<u-icon :name="require('@/static/images/common/close.png')"></u-icon>
							<text>取消公开</text>
						</view>
					</view>
				</view>
				<view class="mySec_list_item_cont">
					<view class="item_text">
						人如果没有了希望和梦想，那么跟咸鱼有什么区别？人如果心里除了工作还是工作，那人生还有什么意义？
					</view>
					<view class="item_images">
						<u-lazy-load 
						:image="require('@/static/images/common/test_pic.png')"></u-lazy-load>
					</view>
				</view>
				<view class="save_diss_wrap">
					<view class="zhanwei"></view>
					<view class="save_diss">
						
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
				
			}
		},
		methods:{
		}
	}
</script>

<style lang="scss">
	.mySec{
		width: 194rpx !important;
		margin: 30rpx 0;
		.mySec_list{
			&_item_top{
				display: flex;
				justify-content: space-between;
				align-items: center;
			}
		}
	}
</style>
