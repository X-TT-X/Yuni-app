<template>
	<view>
		<!-- 轮播图 -->
		<u-swiper :list="banner" previousMargin="30" nextMargin="30" circular height="360rpx" indicator></u-swiper>
		<!-- 板块 -->
		<view class="section-menu">
			<u-grid col="4">
				<u-grid-item>
					<u--image :src="require('@/static/selection/section-1.png')" width="164rpx"
						height="164rpx"></u--image>
					<view class="text">
						<u--text text="本家推荐" color="#333" size="24rpx" align="center"></u--text>
					</view>
				</u-grid-item>
				<u-grid-item>
					<u--image :src="require('@/static/selection/section-2.png')" width="164rpx"
						height="164rpx"></u--image>
					<view class="text">
						<u--text text="挑选师推荐" color="#333" size="24rpx" align="center"></u--text>
					</view>
				</u-grid-item>
				<u-grid-item>
					<u--image :src="require('@/static/selection/section-3.png')" width="164rpx"
						height="164rpx"></u--image>
					<view class="text">
						<u--text text="私物推荐" color="#333" size="24rpx" align="center"></u--text>
					</view>
				</u-grid-item>
				<u-grid-item>
					<u--image :src="require('@/static/selection/section-4.png')" width="164rpx"
						height="167rpx"></u--image>
					<view class="text">
						<u--text text="本家LOOK" color="#333" size="24rpx" align="center"></u--text>
					</view>
				</u-grid-item>
			</u-grid>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				banner: [
					require('@/static/selection/banner-1.png'),
					require('@/static/selection/banner-2.png'),
				],
			}
		},
		methods: {

		}
	}
</script>

<style>
	.section-menu {
		margin: 47rpx 0;
	}

	.section-menu .text {
		margin-top: 22rpx;
	}
</style>