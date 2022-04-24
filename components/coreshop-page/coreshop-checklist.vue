<template>
	<view class="check-list" v-if="checkList.length > 0">
		<u-tabs 
			:current="current"
			active-color="#bb0000"
			inactive-color="#333"
			:list="checkList" 
			height="60rpx" 
			bg-color="#fff"
			@change="typeChange"
			@click="selectType">
			<view
				slot="right"
				style="padding-left: 4px;"
				@tap="$u.toast('插槽被点击')">
				更多
			</view>
		</u-tabs>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				current:0,
				checkList: [{
                    name: '关注',
                }, {
                    name: '推荐',
                }, {
                    name: '电影'
                }, {
                    name: '科技'
                }, {
                    name: '音乐'
                }, {
                    name: '美食'
                }, {
                    name: '文化'
                }, {
                    name: '财经'
                }, {
                    name: '手工'
                }]
			}
		},
		props:{
			// checkList:{
			// 	type:Array,
			// 	default:[]
			// }
		},
		methods:{
			selectType(e){
				this.current = e
			},
			typeChange(e){
				this.current = e
			}
		}
	}
</script>

<style>
	.check-list{
		width: 100%;
		height: 60rpx;
		line-height: 60rpx;
		background-color: #fff;
	}
</style>
