<template>
	<view class="content">
		<view class="kefu" v-on:click="show" v-if="!isShow">
			<image src="../../static/我的_填充(my_fill)_爱给网_aigei_com.png" class="head"></image>
			<view class="namew">Alan</view>
			<view class="wenzi">Hi,what can I do for you?</view>
		</view>
		<view class="commu" v-if="isShow">
			<view class="hengfu">
				<view class="shut" v-on:click="show">
					&ltcir;
				</view>
				<view class="namen">Alan</view>
				<view class="xingxi">
					...
				</view>
				<view class="hengfuwai">
					<image src="../../static/我的_填充(my_fill)_爱给网_aigei_com.png" class="head1"></image>
					<view class="wenzi1k">
						<view class="wenzi1">Hi,what can I do for you?</view>
					</view>
				</view>
			</view>
			<view class="kun">
				<image src="../../static/语音2_爱给网_aigei_com.png" class="zuotu"></image>
				<input class="inputkun">
					
				</input>
				<button class="fasaong">发送</button>
				<image src="../../static/加号（圆圈）_爱给网_aigei_com.png" class="youtu"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return{
				isShow:false
			}
		},
		methods: {
			show(){
				this.isShow = !this.isShow;
				console.log(111);
			}
		}
	}
</script>

<style>
	.namen{
		position: absolute;
		font-weight: bold;
		font-size: 20px;
		top: 10px;
		left: 43%;
	}
	.namew{
		position: absolute;
		top: 10px;
		left: 70px;
		font-weight: bold;
		font-size: 22px;
	}
	.zuotu{
		position: absolute;
		bottom: 2px;
		width: 30px;
		height: 30px;
		left: 0;
	}
	.youtu{
		position: absolute;
		bottom: 2px;
		width: 30px;
		height: 30px;
		right: 2px;
	}
	.kun{
		position: absolute;
		background-color: rgba(50, 50, 50,0.1);
		bottom: 0;
		height: 40px;
		width: 100%;
	}
	.inputkun{
		position: absolute;
		width: 74%;
		border: 4px solid #fff ;
		left: 30px;
		border-radius: 3%;
		background-color: #fff;
		bottom: 3px;
	}
	.fasaong{
		position: absolute;
		width: 50px;
		bottom: 0px;
		height: 35px;
		right: 35px;
		font-size: 16px;
		padding: 0 3px 5px 3px;
		background-color: limegreen;
		font-weight: 800;
	}
	.hengfuwai{
		position: absolute;
		display: block;
		top: 50px;
	}
	.hengfu{
		position: relative;
		top: 0;
		width: 100%;
		height: 45px;
		background-color: rgba(50, 50, 50,0.5);
	}
	.xingxi{
		position: absolute;
		right: 0;
		top: 0;
		width: 35px;
		height: 35px;
		border-radius: 50%;
		text-align: center;
		font-size: 30px;
		font-weight: bold;
		line-height: 25px ;
	}
	.shut{
		position: absolute;
		left: 0;
		top: 0;
		width: 35px;
		height: 35px;
		border-radius: 50%;
		text-align: center;
		font-size: 30px;
		font-weight: bold;
	}
	.commu{
		background-color: white;
		width: 100%;
		height: 100%;
		
	}
	.kefu{
		position: relative;
		display: inline-block;
		width: 100%;
		height: 10%;
		border-top: 3px solid #fff;
		border-bottom: 3px solid #fff;
		top: 0;
		margin: 0 auto;
		background-color: aliceblue;
	}
	.head{
		left: 0;
		width: 60px;
		height: 60px;
		top: 10px;
	}
	.head1{
		left: 0;
		width: 60px;
		height: 60px;
		top: 10px;
		display: block;
	}
	.wenzi{
		position: absolute;
		top: 45px;
		left: 70px;
		color: #8a8a8a;
		font-size: 18px;
	}
	.content {
		width: 100%;
		height: 100%;
		background-image: url('data:image/png;base64,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');
		background-repeat: no-repeat;
		background-size: 100% 100%;
	}
	.wenzi1{
		
	}
	.wenzi1k{
		height: 50px;
		background-color: rgba(50, 50, 50,0.1);
		line-height: 25px;
		border-radius: 0 16% 16% 16%;
		text-indent: 10px;
		font-size: 20px;
		padding: 8px;
		display: block;
		margin: 10px 0 2px 50px;
	}
	

</style>
