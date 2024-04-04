<template>
	<view class="content">
		<view v-if="isShow5" class="matching">
			<input class="inputkun1" placeholder="输入开始时间" v-model="start"></input>
			<input class="inputkun2" placeholder="输入结束时间" v-model="end"></input>
			<button class="wancheng" v-on:click="showTan5();showTan6()">完成</button>
			</view>
		<view v-if="isShow3" class="lvyou" >
			<view class="zibian" >选择出发城市</view>
			<image  src="../../static/city.jpg" class="lvyou" v-on:click="showTan3();showTan4()"></image>
		</view>
		<view v-if="isShow4" class="lvyou" >
			<view class="zibian" >选择抵达城市</view>
			<image  src="../../static/city.jpg" class="lvyou" v-on:click="showTan4();change()"></image>
		</view>
		<view v-if="isShow2" class="lvyou" >
			<view class="guanbi" v-on:click="showTan2()">&ltcir;</view>
			<image  src="../../static/旅游攻略.jpg" class="lvyou"></image>
		</view>
		<image class="logo" src="/static/小飞机2.png"></image>
		<view class="text-area">
			<button class="match" v-on:click="showTan">开始匹配</button>
			<view class="city" v-on:click="showTan3" v-if="chan">选择城市</view>
			<view class="city" v-on:click="showTan3" v-if="!chan">天津 to 长沙</view>
			<view class="triangle1"></view>			
			<view class="date" v-on:click="showTan5" v-if="!isShow6">选择偏好</view>
			<view class="date" v-on:click="showTan5" v-if="isShow6">{{start}} to {{end}}</view>
			<view class="triangle2"></view>
		</view>
		<view class="contact">
			<view>联 系 我 们</view><view class="youjian">^</view>			
			</view>
			<view class="menban" v-if="isShow"></view>
			<view class="tanchuang" v-if="isShow">
				<button class="former" v-on:click="showTan1()">普通匹配</button>
				<button class="former" v-on:click="showTan1()">专人匹配（含代买景点票)（VIP）</button>
				<button class="former" v-on:click="showTan2()">查看以往经典案例 (VIP)</button>
				<button class="former4" v-on:click="showTan">关闭</button>
				<view v-if="isShow1" class="matching">
					<view class="matching1"></view>
					<view class="matching2">正在为您匹配 匹配成功后马上通知您</view>
					<view class="matching3">您的伴旅已经在赶来的路上了</view>
					<button class="matching4" v-on:click="showTan1()">OK</button>
				</view>
			</view>
	</view>
	
	
</template>

<script>
	export default {
		data() {
			return{
				isShow:false,
				isShow1:false,
				isShow2:false,
				isShow3:false,
				isShow4:false,
				isShow5:false,
				isShow6:false,
				chan:true,
				start:'',
				end:''
			}
		},
		methods: {
			showTan(){
				this.isShow = !this.isShow;
			},
			showTan1(){
				this.isShow1 = !this.isShow1;
			},
			showTan2(){
				this.isShow2 = !this.isShow2;
			},
			showTan3(){
				this.isShow3 = !this.isShow3;
			},
			showTan4(){
				this.isShow4 = !this.isShow4;
			},
			showTan5(){
				this.isShow5 = !this.isShow5;
			},
			showTan6(){
				this.isShow6 = !this.isShow6;
			},
			change(){
				this.chan = !this.chan;
			}
		}
	}
</script>

<style>
	@Keyframes donut-spin {
	   0% {
	     transform: rotate(0deg);
	   }
	 
	   100% {
	     transform: rotate(360deg);
	   }
	}
	.inputkun1{
		position: absolute;
		bottom: 200px;
		width: 75%;
		border: 4px solid #fff ;
		left: 30px;
		border-radius: 3%;
		background-color: #fff;
	}
	.inputkun2{
		position: absolute;
		bottom: 130px;
		width: 75%;
		border: 4px solid #fff ;
		left: 30px;
		border-radius: 3%;
		background-color: #fff;
	}
	.wancheng{
		position: absolute;
		bottom: 50px;
		font-size: 20px;
		font-weight: bold;
		left: 110px;
	}
	.zibian{
		left: 100px;
		top: 0;
		z-index: 4;
		font-weight: 500;
		position: absolute;
		font-size: 20px;
		color: orange;
		margin: 0;
		padding: 0;
		filter: blur(0.6px);
	}
	.guanbi{
		left: 0;
		top: 0;
		z-index: 4;
		font-weight: bold;
		position: absolute;
		font-size: 20px;
		color: #979797;
		margin: 0;
		padding: 0;
	}
	.lvyou{
		width: 100%;
		height: 100%;
		z-index: 3;
		position: absolute;
		display: inline-block;
	}
	 .matching{
		 z-index: 2;
		 display: inline-block;
		 width: 300px;
		 height: 300px;
		 bottom: 100px;
		 left: 10px;
		 background-color: #eeeeee;
		 position: absolute;
		 border-radius: 25%;
	 }
	.matching1 {
	   display: inline-block;
	   border: 15px solid rgba(0, 0, 0, 0.1);
	   border-left-color: orange;
	   border-radius: 50%;
	   width: 120px;
	   height: 120px;
	   animation: donut-spin 1.2s linear infinite;
	   position: absolute;
	   left: 25%;
	   bottom: 40%;
	   }
	.matching2{
		left: 8%;
		bottom: 25%;
		position: absolute;
		font-size: 16px;
		font-weight: bold;
	}
	.matching3{
		position: absolute;
		left: 15%;
		bottom: 90%;
		font-weight: 500;
		color: darkorange;
	}
	.matching4{
		position: absolute;
		bottom: 8%;
		left: 34%;
		color: orange;
		font-weight: 1000;
		background-color: limegreen;
		width: 100px;
		font-size: 20px;
	}

	.former4{
		display: flex;
		position: absolute;
		bottom: 0;
		right: 0;
		background-color: orange;
		font-weight: bold;
		color: #fff;
		background-color: rgba(0,0,0,0.7);
		font-size: 15px;
	}
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: #fcff00;
		width: 100%;
		height: 100%;
		background-image: url('data:image/png;base64,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');
		background-repeat: no-repeat;
		background-size: cover;
	}

	.logo {
		height: 450rpx;
		width: 600rpx;
		display:block;
		margin: 200rpx auto 0rpx;
		padding: 0 0 50rpx 0;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	.match{
		background-color: transparent;
		display: inline-block;
		margin: 0rpx auto 300rpx;
		border-radius: 10%;
		border-color: orange;
		size: 60px;
		box-shadow: 0 10px 15px 0 rgba(0,0,0,0.2), 0 8px 20px 0 rgba(0,0,0,0.19);
		font-size: 24px;
		padding: 0px 100px 0px;
		font-weight: 925;
		border: 8px solid orange;
		color: orange;
		letter-spacing: 3px;
		
	}
	.contact{
		width: 100%;
		height: 100rpx;
		color: #fff;
		background-color: orange;
		border-radius: 20% 20% 0 0;
		text-align: center;
		font-weight:800;
		font-size: 25px;
	}
	.youjian{
		position: absolute;
		line-height: 35px;
		bottom: 15px;
		right: 20rpx;
		text-shadow: #fcff00;
		font-size: 32px;
		font-weight: bold;
	}
	.city{
		position: absolute;
		bottom: 180px;
		width: 280px;
		background-color: #eeeeee;
		height: 50px;
		border-radius: 5% 5% 15% 15%;
		opacity: 90%;
		text-indent: 5px;
		font-weight: bold;
		color: #8a8a8a;
		box-shadow: 5px 5px #c7c7c7;
		font-size: 25px;
	}
	.date{
		position: absolute;
		bottom: 120px;
		width: 280px;
		background-color:#eeeeee;
		height: 50px;
		border-radius: 5% 5% 15% 15%;
		opacity: 90%;
		text-indent: 5px;
		font-weight: bold;
		color: #8a8a8a;
		box-shadow: 5px 5px #c7c7c7;
		white-space: pre;
		font-size: 25px;
	}
	.triangle1{
		position: absolute;
		bottom: 205px;
		right: 105px;
		width: 0;
		height: 0;
		border-left: 10px solid transparent;
		border-bottom: 10px solid transparent;
		border-right: 10px solid #fff;
		border-top: 10px solid #fff;
	}
	.triangle2{
		position: absolute;
		bottom: 145px;
		right: 105px;
		width: 0;
		height: 0;
		border-left: 10px solid transparent;
		border-bottom: 10px solid transparent;
		border-right: 10px solid #fff;
		border-top: 10px solid #fff;
	}
	.menban{
		position: fixed;
		left: 0;
		top: 0;
		background-color: rgba(0,0,0,0.4);
		width: 100%;
		height: 100%;
	}
	.tanchuang{
		position: fixed;
		left: 0;
		bottom: 0;
		background-color: orange;
		width: 100%;
		height: 60%;
	}
	.former{
		font-weight: bold;
		border:3px solid #000 ;
		line-height: 65px;
	}
	
</style>
