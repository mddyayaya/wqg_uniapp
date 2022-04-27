<template>
	<view>
        <!--提示框组件-->
        <u-toast ref="uToast" />
        <!--无网络组件-->
        <u-no-network></u-no-network>
        <u-navbar :is-back="false" title="观澜" :background="background" :title-color="titleColor"></u-navbar>
		<!-- 观澜模块化组件 -->
		<coreguanlan></coreguanlan>
		<!-- </view> -->
        <!--版权组件-->
        <copyright></copyright>
        <!--返回顶部组件-->
        <u-back-top :scroll-top="scrollTop" :duration="500"></u-back-top>

        <!--弹出框-->
        <!--<coreshop-modal-img :show="modalShow"  :src="$globalConstVars.apiFilesUrl+'/static/images/empty/reward.png'" @imgTap="imgTap" @closeTap="closeTap" />-->
        <!-- 登录提示 -->
        <coreshop-login-modal></coreshop-login-modal>
	</view>
</template>

<script>
    import coreguanlan from '@/components/coreguanlan-page/coreguanlan.vue';
	export default {
		data() {
			return {
                background: this.$coreTheme.mainNabBar.background,
                titleColor: this.$coreTheme.mainNabBar.titleColor,
			}
		},
		components:{coreguanlan},
		methods: {
			
		}
	}
</script>

<style>

</style>
