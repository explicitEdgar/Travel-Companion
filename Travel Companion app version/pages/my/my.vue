<template>
	<view class="content">
		<view class="yetou">
			<image src="../../static/我的_填充(my_fill)_爱给网_aigei_com.png" class="head"></image>
		<view class="mycontent">
			<view class="wenzi1">我的满意度等级为1级</view>
		<view class="wenzi1">距离下一级还有：</view>
		<view class="wenzi2">15</view>
		<view class="g-container">
		    <view class="g-progress"></view>
		</view>
		</view>
		</view>
		
		<view class="but">
			<!-- <view class="iconfont icon-kaitongfuwu"></view> -->
			<button class="xiugai0">升级为VIP用户                    &gt;</button>
		<button class="xiugai">修改个人信息                      &gt;</button>
		<button class="xiugai">退出登录                             &gt;</button>
		<button class="xiugai1">关于我们                             &gt;</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.yetou{
		background-color: #ffffff;
	}
	.content {
		align-items: center;
		background-color: #f1f1f1;
		width: 100%;
		height: 100%;
		/* background-image: url("/static/OIP-C (2).png"); */
		background-repeat: no-repeat;
		background-size: 100% 100%;
		z-index: -1;
		}
	.wenzi1{
		font-weight: bold;
		font-size: 25px;
		color: #666666;
	}
	.wenzi2{
		font-weight: bold;
		font-size: 25px;
		color: orange;
	}
	.xiugai0{
		display: inline-block;
		bottom: 0;
		width: 100%;
		line-height: 50px;
		color: #666666;
		font-weight: bold;
		/* border: 5px solid #f1f1f1 ; */
		border-right: 0;
		border-left: 0;
		font-size: 20px;
		margin: 5px auto 60px;
		background-color: #ffffff;
		border-radius: 5%;
		left: 0px;
		white-space: pre;
	}
	.xiugai1{
		display: inline-block;
		bottom: 0;
		width: 100%;
		line-height: 50px;
		color: #666666;
		font-weight: bold;
		/* border: 5px solid #f1f1f1 ; */
		border-right: 0;
		border-left: 0;
		font-size: 20px;
		margin: 60px auto 3px;
		background-color: #ffffff;
		border-radius: 5%;
		left: 0px;
		white-space: pre;
	}
	.xiugai{
		display: inline-block;
		bottom: 0;
		width: 100%;
		line-height: 50px;
		color: #666666;
		font-weight: bold;
		/* border: 5px solid #f1f1f1 ; */
		border-bottom: 0px;
		border-right: 0;
		border-left: 0;
		font-size: 20px;
		margin: 3px auto;
		background-color: #ffffff;
		border-radius: 5%;
		left: 0px;
		white-space: pre;
	}
	.g-progress {
	
	    width: 240px;
	
	    height: 25px;
	
	    border-radius: 25px;
	
	    background: linear-gradient(45deg, #FFA500, #FFFF00 70%, transparent 0);
	
	    border: 3px solid #555;
		
		display: inline-block;
		
		margin: 0 auto;
	
	}
	.head{
		width: 150px;
		height: 150px;
		display: block;
		margin: 0 auto;
	}
	.mycontent{
		text-align: center;
	}
	.g-container{
		
	}
	.but{
		font-size: 0;
	}
	
	
</style>
