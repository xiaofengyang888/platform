<template>
	<view class="container">
		<!-- logo -->
		<view class="logo">
			LOGO
		</view>
		<!-- title text 宜平台项目申请 -->
		<view class="platForName">
			宜平台项目申请
		</view>
		
		<!-- 初宝 select -->
		<button class="loginBtn" @click="Chubao">
			初宝项目登录入口
		</button>
		
		<!-- 鸿运 select -->
		<button class="loginBtn" @click="Hongyun">
			鸿运项目登录入口
		</button>
		
		<view style="height: 220px">
			
		</view>
		<!-- version -->
		<view class="version">
			宜平台 v 1.0 版本
		</view>
	</view>
</template>

<script>
	
	export default {
		data() {
			return {
				fullHeight: "",
				windWidth: "",
				pageData: {pageId: 1, pageTitle: "初宝项目申请"},
			}
		},
		
		onLoad() {
			uni.getSystemInfo({success: res=> {
				const windowHeight  = res.windowWidth + "px";
				this.windWidth = res.windowWidth + "px";
				console.log("1111111111111 ", this.windWidth);
		},
		
		mounted(){
			
			}})
		},
		
		
		
		methods: {
			Chubao(){
				// : "/pages/loginPage/loginPage?pageId=1&title=初宝项目申请"
				console.log("选择初宝");
				// this.pageData.pageId = 1;
				// this.pageData.pageTitle = "初宝项目申请";
				
				// let data = encodeURIComponent(JSON.stringify(this.pageData));
				
				let loginUrl = "/pages/loginPage/loginPage?id=1&title=初宝项目申请";
				// let loginUrl = "/pages/loginPage/loginPage?data=${encodeURIComponent(JSON.stringify(pageData))}";
				uni.navigateTo({url: loginUrl});
			},
			
			Hongyun(){
				console.log("选择鸿运");
				// this.pageData.pageId = 1;
				// this.pageData.pageTitle = "鸿运项目申请";
				// let data = JSON.stringify(this.pageData);
				
				let loginUrl = "/pages/loginPage/loginPage?id=2&title=鸿运项目申请";
				uni.navigateTo({
					url:loginUrl
				})
			}
		}
	}
</script>

<style>
	.container{
		flex-direction: column;
		/* background-color: aquamarine; */
		height: 700px;
		align-items: center;
		justify-content: center;
		
	}
	
	.logo{
		text-align: center;
		height: 200rpx;
		width: 378px;
		margin-left: 3px;
		font-size: 46px;
		margin-top: 100rpx;
	}
	
	.platForName{
		/* background-color: yellow; */
		text-align: center;
		font-size: 40px;
		height: 100px;
		width: 400px;
		
		/* background-color: #4095E5; */
		margin-top: 30px;
	}
	
	.loginBtn{
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 24px;
		width: 300px;
		height: 80px;
		margin-top: 80px;
		background-color: #4095E5;
		color: #FFFFFF;
	}
	
	.version{
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 22px;
		color: #C0C0C0;
		margin-bottom: 10px;
	}
</style>
