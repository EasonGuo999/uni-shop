<template>
	<view class='scroll-view-wrapper'>
		<scroll-view class='scroll-view-left' scroll-y :style='{height:wh + "px"}'>
			<view class='left-scroll-view-item active'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
			<view class='left-scroll-view-item'>left</view>
		</scroll-view>
		
		<scroll-view class='scroll-view-right' scroll-y :style='{height:wh + "px"}'>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
			<view>right</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				wh:0
			};
		},
		onLoad(){
			const sysInfo=uni.getSystemInfoSync()
			this.wh=sysInfo.windowHeight
		}
	}
</script>

<style lang="scss">
	.scroll-view-wrapper{
		display:flex
	}
	.left-scroll-view-item{
		background-color: #f7f7f7;
		line-height:60px;
		text-align:center;
		font-size:12px;
	
		&.active{
			background-color: #fff;
			position:relative;
			
			&::before{
				content:'';
				display:block;
				width: 3px;
				height:30px;
				background-color: #c00000;
				position:absolute;
				top:50%;
				left:0;
				transform:translateY(-50%)
			}
		}
	}
</style>
