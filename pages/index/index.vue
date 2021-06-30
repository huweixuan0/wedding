<template>
	<view class="page bg-blue">
		<cu-custom>
			<block slot="content">记录一些小事zzz</block>
		</cu-custom>
		<view class="labler">
				<view>
					<view class="cu-avatar lg round margin-left" style="background-image:url(https://ossweb-img.qq.com/images/lol/web201310/skin/big25002.jpg);"></view>
				</view>
				<view>
					<view>在一起已经</view>
					<view><text>{{xdd}}</text><text>天啦</text></view>
				</view>
				<view>
					<view class="cu-avatar lg round margin-left" style="background-image:url(https://ossweb-img.qq.com/images/lol/web201310/skin/big25002.jpg);"></view>
				</view>
		</view>
		<view class="labler" style="width: 69%;">
				<text>距离结婚还有：</text><text>{{dd}}</text><text>天</text><text>{{hh}}</text><text>时</text><text>{{mm}}</text><text>分</text>
				<text>{{ss}}</text><text>秒</text>
		</view>
		<navigator :url="'/pages/timeline/timeline'" navigateTo>
		<view class="right">
			<view class="cu-capsule round">
				<view class='cu-tag bg-red '>
					<text>&</text>
					<text class='cuIcon-likefill'></text>
					<text>&</text>
				</view>
					<view class="cu-tag line-red">
						时光机
					</view>
			</view>
		</view>
		</navigator>
		<!-- <view class="box">
			<view>
				<view>
					<text class="text-xsl text-green cuIcon-calendar"></text>
				</view>
				<view>纪念日</view>
			</view>
			<view>
				<view></view>
				<view>时光机</view>
			</view>
			<view>
				<view></view>
				<view>日记本</view>
			</view>
		</view> -->
	</view>
	
	
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				dd:"",
				hh:"",
				mm:"",
				ss:"",
				xdd:""
			}
		},
		onLoad() {
			this.countTime();
			this.together();
		},
		methods: {
			countTime(){
					//获取当前时间
		            var date = new Date();
		            var now = date.getTime();
		            //设置截止时间
		            var str="2021/10/16 12:00:00";
		            var endDate = new Date(str);
		            var end = endDate.getTime();
					
		            //时间差
		            var leftTime = end-now;
					//console.log(leftTime)
		            //定义变量 d,h,m,s保存倒计时的时间
		            var d,h,m,s;
		            if (leftTime>=0) {
		                this.dd = Math.floor(leftTime/1000/60/60/24);
		                this.hh = Math.floor(leftTime/1000/60/60%24);
		                this.mm = Math.floor(leftTime/1000/60%60);
		                this.ss = Math.floor(leftTime/1000%60);
		            }
					//console.log(this.dd)
		            //递归每秒调用countTime方法，显示动态时间效果
		            setTimeout(this.countTime,1000);
			},
			together(){
				//获取当前时间
				var date = new Date();
				var now = date.getTime();
				
				//在一起的时间
				var str = "2020/11/17 12:00:00";
				var start = new Date(str);
				
				//时间差
				var leftTime = now-start;
				this.xdd = Math.floor(leftTime/1000/60/60/24);
			}
		}
	}
</script>

<style lang="scss">
.page{
	height: 100vh;
}

.labler{
	background-color: rgba($color: #fff, $alpha: .3);
	margin-top: 50upx;
	height: 130upx;
	width: 60%;
	display: flex;
	border-radius: 0 100upx 100upx 0;
	overflow: hidden;
	align-items: center;
	justify-content: space-around;
	&>view:nth-child(2){
		text-align: center;
	}
}
.right{
	margin-top:100upx;
	float: right;
	margin-right: 45upx;
}
// .box{
// 	position: absolute;
// 	bottom: 60upx;
// 	left: 0upx;
// 	width: 100%;
// 	display: flex;
// 	justify-content: space-around;
// 	&>view{
// 		margin-top:30upx;
// 		width: 150upx;
// 		height: 150upx;
// 		background-color: #fff;
// 		border-radius: 100upx;
// 		text-align: center;
// 		color: #000;
// 	}
// 	&>view:nth-child(2){
// 		margin-top:0upx;
// 	}
	
// }
</style>
