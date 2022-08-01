<template>
	<view class="content">
		<!-- 头部 -->
		<view class="top">
			<image class="logo" src="/static/logo2.png"></image>
			<view class="topleft">
				<u-icon size="40" name="search"></u-icon>
				<button class="topbut">下载APP | 登录</button>
			</view>
		</view>
		<!-- 导航栏 -->
		<view class="nav">
			<view class="navbox">
				<view class="topn">
					<text>首页</text>
					<text>免费课</text>
					<text>实战课</text>
					<text>体系课</text>
				</view>
				<view class="botn">
					<text>专栏</text>
					<text>手记</text>
					<text>慕课教程</text>
				</view>
			</view>
			
		</view>
		<!-- uView选项卡 -->
		<view class="tab">
			<u-tabs :list="list" :is-scroll="false" :current="current" @change="change()"></u-tabs>
		</view>
		<!-- 内容盒子布局 -->
		<view class="container">
			<view class="a">
				<image src="../../static/1.jpg" mode=""></image>
				<view class="b">
					<text class="title">73人学习 · 新上好课</text>
					<text class="red">￥11999</text><text class="line">￥14999</text>
					<u-tag style="width: 60px;" text="首期特惠" size="mini" mode="dark" bg-color="white" border-color="red" color="red"/>
				</view>
			</view>
			<view class="a">
				<image src="../../static/2.png" mode=""></image>
				<view class="b">
					<text class="title">73人学习 · 新上好课</text>
					<text class="red">￥11999</text><text class="line">￥14999</text>
					<u-tag style="width: 60px;" text="首期特惠" size="mini" mode="dark" bg-color="white" border-color="red" color="red"/>
				</view>
			</view><view class="a">
				<image src="../../static/3.png" mode=""></image>
				<view class="b">
					<text class="title">73人学习 · 新上好课</text>
					<text class="red">￥11999</text><text class="line">￥14999</text>
					<u-tag style="width: 60px;" text="首期特惠" size="mini" mode="dark" bg-color="white" border-color="red" color="red"/>
				</view>
			</view><view class="a">
				<image src="../../static/4.png" mode=""></image>
				<view class="b">
					<text class="title">73人学习 · 新上好课</text>
					<text class="red">￥11999</text><text class="line">￥14999</text>
					<u-tag style="width: 60px;" text="首期特惠" size="mini" mode="dark" bg-color="white" border-color="red" color="red"/>
				</view>
			</view><view class="a">
				<image src="../../static/5.png" mode=""></image>
				<view class="b">
					<text class="title">73人学习 · 新上好课</text>
					<text class="red">￥11999</text><text class="line">￥14999</text>
					<u-tag style="width: 60px;" text="首期特惠" size="mini" mode="dark" bg-color="white" border-color="red" color="red"/>
				</view>
			</view>
		</view>
	</view>
</template>


<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		data() {
			return {
				list: [{
					name: '全部'
				}, {
					name: '零基础'
				}, {
					name: '进阶课',
					count: 5
				}],
				current: 0
			}
		},
		methods: {
			change(index) {
				this.current = index;
			}
		}
	}
</script>

<style lang="scss">
	.content{
		background: #eff1f3;
		width: 100%;
		height: 100vh;
		border:1px solid red;
		flex-wrap: wrap;
		.top{
			width: 95%;
			height: 80px;
			display: flex;
			justify-content:space-between;
			align-items: center;
			padding:0 20px;
			margin:0 auto;
			.logo{
				width: 100px;
				height:30px;
			}
			.topleft{
				display: flex;
				align-items: center;
				.topbut{
					background: rgba(255, 0, 0, .1);
					border-radius: 40px;
					outline: none;
					border:none;
					color: rgba(255, 0, 0, 1);
				}
			}
		}
		.nav{
			width: 95%;
			margin:0 auto;
			.navbox{
				font-weight: bold;
				color: #71777d;
				.topn{
					width:400px;
					height: 50px;
					display: flex;
					justify-content: space-around;
					line-height: 50px;
				}
				.botn{
					width: 300px;
					height: 50px;
					display: flex;
					justify-content: space-around;
					line-height: 50px;
				}
			}
		}
		.tab{
			width: 98%;
			margin:10px auto;
			
		}
		.container{
			width: 95%;
			display: flex;
			flex-wrap: wrap;
			height: 100vh;
			
			margin:0 auto;
			// 内容布局
			.a{
				overflow: hidden;
				width:45%;
				background: white;
				border-radius: 40px;
				image{
					
					width: 100%;
				}
				margin:10px;
			}
			// 文字布局
			.b{
				
				padding:20px;
				.title{
					font-size: 13px;
					display: block;
					color: #aaa;
					
				}
				.line{
					color: #aaa;
					
					text-decoration: line-through;
					margin:10px 0;
				}
				.red{
					font-size: 20px;
					color: red;
					text-decoration: none;
				}
			}
		}
	}
</style>
