<template>
	<view class='swiper'>
		<swiper indicator-dots indicator-color='white' indicator-active-color='grey'
				autoplay interval='3000' circular>
			<swiper-item v-for='item in swiperList' :key='item.id'>
				<navigator :url='`/subpkg/goods_detail/goods_detail?id=${item.id}`'>
					<image :src='item.src'></image>
				</navigator>
			</swiper-item>
		</swiper>
	</view>	
	
	<view class='nav-wrapper'>
		<view v-for='item in navList'  class='nav-item' :key='item.id'>
			<navigator :url='`/subpkg/goods_detail/goods_detail?id=${item.id}`'>
				<image :src='item.src' class='nav-img'></image>
				<view class='nav-name'>{{item.name}}</view>
			</navigator>
		</view>
	</view>
	
	<view class='floor-wrapper'>
		<view class='floor-item' v-for='(item,index) in floorList' :key='index' @click='toFloorHandler'>
			<image :src='item.src' class='floor-title'></image>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiperList:[
					{	
						id:1,
						src:'../../static/swiper_photos/jd1.jpg'
					},
					{
						id:2,
						src:'../../static/swiper_photos/jd2.jpg'
					},{
						id:3,
						src:'../../static/swiper_photos/jd3.jpg'
					}
				],
				navList:[
					{
						id:1,
						name:'分类',
						src:'../../static/navList/nav1.jpg'
					},
					{
						id:2,
						name:'秒杀拍',
						src:'../../static/navList/nav2.jpg'
					},
					{
						id:3,
						name:'超市购',
						src:'../../static/navList/nav3.jpg'
					},
					{
						id:4,
						name:'母婴品',
						src:'../../static/navList/nav4.jpg'
					}
				],
				floorList:[
					{
						id:1,
						name:'phone1',
						src:'../../static/floor/floor1.jpg',	
					},
					{
						id:2,
						name:'phone2',
						src:'../../static/floor/floor2.jpg',	
					},
					{
						id:3,
						name:'phone3',
						src:'../../static/floor/floor3.jpg',	
					},
					{
						id:4,
						name:'phone4',
						src:'../../static/floor/floor4.jpg',	
					}
				]
			};	
		},
		onLoad(){
			
		},
		methods:{
		   toFloorHandler(){
			   uni.navigateTo({
				   url:'/subpkg/sub_floor/sub_floor'
			   })
		   }
		}
	}
</script>

<style lang="scss">
	swiper-item image{
		width: 100%;
	}
	.nav-wrapper{
		margin-top:10rpx;
		width:100%;
		display:flex;
		justify-content:space-evenly
	}
	.nav-item{
		width:130rpx;
		height: 100rpx;
	}
	.nav-item navigator{
		display:flex;
		flex-direction: column;
		align-items:center;	
	}
	.nav-img{
		width:100rpx;
		height:100rpx;	
	}
	.nav-name{
		font-size:25rpx
	}
	
	.floor-wrapper{
		width:100%;
		display:flex;
		flex-wrap:wrap;
	}
	.floor-item{
		width:50%;
	}
	.floor-item image{
		width:100%;

	}
</style>
