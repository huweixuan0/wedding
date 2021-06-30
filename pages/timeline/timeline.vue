<template>
	<view>
		<cu-custom bgColor="bg-gradual-pink" :isBack="true"><block slot="backText">返回</block><block slot="content">时间轴</block></cu-custom>
		<view class="cu-timeline">
			<view class="cu-time">21-01-16</view>
			<view class="cu-item cur cuIcon-noticefill">
				<view class="content bg-green shadow-blur">
					<text>22:22</text> 我们订婚啦
				</view>
			</view>
		</view>
		<view class="cu-timeline">
			<view class="cu-time">21-01-16</view>
			<view class="cu-item cur cuIcon-noticefill">
				<view class="content bg-green shadow-blur">
					<text>22:22</text> 看门楼
				</view>
			</view>
		</view>
		<view class="cu-timeline">
			<view class="cu-time">21-01-16</view>
			<view class="cu-item text-blue">
				<view class="bg-blue content">
					<text>父母一起聊我们的事情</text>
				</view>
			</view>
		</view>
		<view class="cu-timeline">
			<view class="cu-time">20-11-28</view>
			<view class="cu-item text-red cuIcon-noticefill">
				<view class="content bg-red shadow-blur">
					<text>这天很重要，</text>宝宝带我去见叔叔阿姨啦，好紧张
				</view>
			</view>
		</view>
		<view class="cu-timeline">
			<view class="cu-time">20-11-28</view>
			<view class="cu-item">
				<view class="content">
					<text>紧张激动的第一次牵着你，原来我们都很爱吃，都很爱笑，嘿嘿嘿</text>
				</view>
			</view>
		</view>

		<view class="cu-timeline">
			<view class="cu-time">20-11-17</view>
			<view class="cu-item">
				<view class="content">
					<view class="cu-capsule radius">
						<view class="cu-tag bg-cyan">晚上</view>
						<view class="cu-tag line-cyan">18:00</view>
					</view>
					<view class="margin-top">初次见面</view>
				</view>
			</view>
			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		}
	}
</script>

<style>

</style>
