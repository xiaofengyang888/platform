<template>
	<view class="container">
		<view class="title"> 新用户注册 </view>
		<!-- v-for="(item, index) in inputTexts" :key="index" -->
		<view class="textInputContainer">
			<view ><input class="textInputItem" placeholder="请输入手机号码"/></view>
			<view><input class="textInputItem" placeholder="请输入姓名"/></view>
			<view><input class="textInputItem" placeholder="请输入登录密码" type="password"/></view>
			<view><input class="textInputItem" placeholder="再次输入登录密码" type="password"/></view>
			
			<uni-combox class="combox" style="border-color: #c6c6c6; border-width: 2px;"
			:candidates="candidates" 
			placeholder="请选择战略大区" 
			v-model="area"></uni-combox>

			
			<uni-combox class="combox"
			:candidates="sales" 
			placeholder="请选择销售大区" 
			v-model="sale"></uni-combox>
			
			<!-- <view><input class="textInputItem" placeholder="请选择销售大区"/></view> -->
			<view class="codeContainer">
				<input class="codeIput" placeholder="请输入验证码"/>
				<button class="getCodeBtn">获取验证码</button>
			</view>
			
			<button class="loginBtn">注册并登录</button>
			
			
		</view>
	</view>
		
</template>

<script>
	
	export default {
		data() {
			return {
				inputTexts: [
					"请输入手机号码",
					"请输入姓名",
					"请输入登录密码",
					"再次输入登录密码",
					"请选择战略大区",
					"请选择销售大区",
					"请输入验证码"
				],
				
				candidates: ['战略一区', '战略二区', '战略三区'],
				area: '',
				
				sales: ['销售一区', '销售二区', '销售三区'],
				sale: ''
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.container{
		height: 1500rpx;
		width: 800rpx;
		/* background-color: aliceblue; */
		display: flex;
		flex-direction: column;
		/* justify-content: center; */
		align-items: center;
	}
	
	.title{
		width: 400rpx;
		height: 100rpx;
		/* background-color: antiquewhite; */
		text-align: center;
		font-size: 24px;
		font-weight: bold;
		margin-top: 100rpx;
		align-items: center;
	}
	
	.textInputContainer{
		width: 800rpx;
		height: 1600rpx;
		/* background-color: azure; */
	}
	
	.textInputItem{
		margin-top: 30px;
		margin-left: 40px;
		padding-left: 16px;
		align-items: center;
		border: 1px solid darkgray;
		color: black;
		font-size: 22px;
		font-weight: 500;
		/* background-color: aliceblue; */
		width: 600rpx;
		height: 80rpx;
	}
	
	.combox{
		width: 600rpx;
		height: 80rpx;
		margin-top: 30px;
		margin-left: 40px;
		border: 3px solid #C6C6C6;
		font-size: 24px;
	}
	
	.codeContainer{
		width: 620rpx;
		height: 100rpx;
		display: flex;
		flex-direction: row;
		align-items: center;
		margin-left: 40px;
		margin-top: 30px;
		border: 2px solid #C6C6C6;
	}
	
	.codeIput{
		width: 400rpx;
		height: 80rpx;
		font-size: 22px;
		text-align: left;
		padding-left: 20rpx;
	}
	
	.getCodeBtn{
		width: 280rpx;
		height: 80rpx;
	}
	
	.loginBtn{
		width: 640rpx;
		height: 100rpx;
		color: #FFFFFF;
		background-color: #4095E5;
		margin-top: 30px;
	}
</style>
