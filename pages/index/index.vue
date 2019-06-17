<template>
	<view class="content">
		<!-- 状态栏 -->
		<view class="status_bar"></view>
		<!-- 搜索框 -->
		<view class="search-bar">
			<view class="school-name">{{ schoolName }}</view>
			<view class="input-div">
				<view class="iconfont iconchazhao"></view>
				{{ placeholder }}
			</view>
		</view>
		<swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="300" :circular="true">
			<swiper-item v-for="(item,index) in swiperList" :key="index">
				<view class="swiper-item">
					<image class="imgs" :src="item.src" mode=""></image>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				schoolName: '天津职业大学',
				placeholder: '资讯、动态、商品',
				swiperList: [
					{src:'../../static/banner/banner001.png',url:'http://baidu.com'},
					{src:'../../static/banner/banner002.png',url:'http://baidu.com'},
					{src:'../../static/banner/banner003.png',url:'http://baidu.com'},
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.search-bar {
		height: 100upx;
		padding: 0 20upx;
		font-size: 28upx;
		display: flex;
		flex-direction: row;
		align-items: center;

		.school-name {
			width: 200upx;
			white-space: nowrap;
			text-overflow: ellipsis;
			overflow: hidden;
			color: $uni-base-color;
		}

		.input-div {
			height: 60upx;
			border-radius: 30upx;
			flex: 1;
			line-height: 60upx;
			padding-left: 20upx;
			color: #999;
			background-color: #f8f8f8;
			cursor: pointer;

			.iconchazhao {
				display: inline-block;
				margin-right: 15upx;
			}
		}
	}

	.swiper {
		margin: 10upx 30upx;
		border-radius: 30upx;
		overflow: hidden;
		.swiper-item,.imgs{
			width: 100%;
			height: 100%;
		}
	}
</style>
