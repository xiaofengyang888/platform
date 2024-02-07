<template>
	<view class="container">
		<view class="logo">
			LOGO
		</view>
		
		<view class="platForName">
			{{mytitle}}
		</view>
		
		<view class="textInputContainer">
			<view class="textInputItem">
				<input class="text" placeholder="请输入手机号"/>
			</view>
			<view class="textInputItem">
				<input class="text" placeholder="请输密码" type="password"/>
			</view>
		</view>
		
		<view class="textButtonView">
			<text class="textButton" @click="register">新人注册</text>
			<text class="textButton" @click="codeLogin">验证码登录</text>
		</view>
		
		<view class="bottomContainer">
			<button class="bottomButton">登录</button>
			<button class="bottomButton">返回选择界面</button>
			<text class="version">宜平台 V1.0 版本 </text>
		</view>
	
	</view>
</template>

<script>
	export default {
		data() {
			return {
				mytitle: "",
			}
		},
		
		onLoad(options) {
			// let data = JSON.parse(decodeURIComponent(options.data));		
			// console.log("data ", options.title);
			this.mytitle = options.title;
		},
		
		mounted() {
			
		},
		
		methods: {
			register(){
				console.log("新用户注册");
				uni.navigateTo({
					url:"/pages/userRegisterPage/userRegisterPage"
				})
			},
			
			codeLogin(){
				console.log("验证码登录");
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
		padding-top: 100px;
		text-align: center;
		height: 200rpx;
		width: 400px;
		font-size: 46px;
		padding-left: 10px;
	}
	
	.platForName{
		display: flex;
		justify-content: center;
		font-size: 40px;
		height: 100px;
		width: 400px;
		margin-top: 40px;
	}
	
	.textInputContainer{
		display: flex;
		flex-direction: column;
	}
	
	.textInputItem{
		margin-top: 20px;
		margin-left: 46px;
		padding-left: 16px;
		align-items: center;
		border: 1px solid darkgray;
		color: black;
		font-size: 22px;
		font-weight: 500;
		/* background-color: aliceblue; */
		width: 300px;
		height: 40px;
	}
	
	.text{
		padding-top: 6px;
	}
	
	.textButtonView{
		display: flex;
		flex-direction: row;
		padding-left: 180px;
	}
	
	.textButton{
		text-decoration:underline;
		color: cornflowerblue;
		border: black;
		background-color: transparent;
		line-height: 40px;
		width: 60;
		padding-left: 20px;
	}
	
	.bottomContainer{
		padding-top: 30rpx;
		width: 400px;
		height: 300px;
	}
	
	.bottomButton{
		width: 600rpx;
		height: 100rpx;
		margin-top: 60rpx;
		text-align: center;
		color: #FFFFFF;
		background-color: #4095E5;
		font-weight: bold;
	}
	
	.version{
		display: flex;
		justify-content: center;
		align-items: center;
		padding-top: 120rpx;
		font-size: 16px;
		color: #C0C0C0;
	}
	
</style>
