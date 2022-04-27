<template>
	<view class="guanlan_wrap">
		<!-- 观澜模块化组件 -->
		<coreshopBar></coreshopBar>
		<coreshopDaren></coreshopDaren>
	</view>
</template>

<script>
    import coreshopBar from './coreguanlanbar.vue';
    import coreshopDaren from './coreguanlandr.vue';
	export default {
		data() {
			return {
                background: this.$coreTheme.mainNabBar.background,
                titleColor: this.$coreTheme.mainNabBar.titleColor,
			}
		},
		components:{
			coreshopBar,
			coreshopDaren
		},
		methods: {
			
		}
	}
</script>

<style>
	.guanlan_wrap{
		width: 100%;
	}

</style>
