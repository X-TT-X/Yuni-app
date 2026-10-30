<template>
	<view>
		<!-- 轮播图 -->
		<u-swiper :list="banner" height="750rpx" indicator img-mode="widthFix"></u-swiper>
		<!-- 商品信息 -->
		<u-cell-group>
			<u-cell>
				<view calss="goods" slot="title">
					<view class="name">
						<u--text text="韩版长款修身连衣裙" size="34rpx" color="#555" lines="2"></u--text>
					</view>
					<view class="word">
						<u--text text="韩版修身" size="26rpx" color="#999" lines="1"></u--text>
					</view>
					<view class="price">
						<u--text text="￥399" size="40rpx" color="#c55a5c" lines="1"></u--text>
					</view>
				</view>
				<view class="comment-data" slot="value">
					<view class="count">
						<u--text text="469" size="36rpx" color="#c55a5c" align="center"></u--text>
					</view>
					<view class="text">
						<u--text text="用户评价" size="24rpx" color="#c55a5c" align="center"></u--text>
					</view>
					<navigator url="" class="link">
						<u-button text="查看评价" size="mini"></u-button>
					</navigator>
				</view>
			</u-cell>
		</u-cell-group>
		<!-- 间隔槽 -->
		<u-gap height="10" bgColor="#f4f4f4"></u-gap>
		<!-- 规格信息 -->
		<u-cell-group>
			<u-cell title="规格数量选择" :is-link="true"></u-cell>
			<u-cell :is-link="true">
				<view class="promotion" slot="title">
					<view>
						<u--text text="1个促销"></u--text>
					</view>
					<view>
						<u--text text="120款爆品满3件8折" color="#c55a5c"></u--text>
					</view>
				</view>
			</u-cell>
			<u-cell title="积分:购买最高可得59积分"></u-cell>
			<u-cell :is-link="true">
				<view class="sevice" slot="title">
					<view class="label">
						<u--text text="服务:"></u--text>
					</view>
					<view class="list">
						<view class="item">
							<u--text text="30天无理由退货" size="24rpx" color="#999"></u--text>
						</view>
						<view class="item">
							<u--text text="48小时快速退款" size="24rpx" color="#999"></u--text>
						</view>
						<view class="item">
							<u--text text="满88元免邮费" size="24rpx" color="#999"></u--text>
						</view>
					</view>
				</view>
			</u-cell>
		</u-cell-group>
		<!-- 间隔槽 -->
		<u-gap height="10" bgColor="#f4f4f4"></u-gap>
		<!-- 用户评论 -->
		<view class="user-comments">
			<u-cell title="用户评价:(536)" valu="99.1% 好评" :is-link="true"></u-cell>
			<!-- 列表 -->
			<view class="list">
				<view class="comment">
					<view class="user">
						<view class="avater">
							<u--image :src="require('@/static/center/avatar.png')" shape="circle" width="80rpx"
								height="80rpx">
							</u--image>
						</view>
						<view class="nickname">
							<u--text text="昵称" size="24rpx" color="#666"></u--text>
						</view>
						<view class="stars">
							<u-rate :value="3.7" active-color="#fab646" readonly></u-rate>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				banner: [
					require('@/static/detail/photo-2.jpg'),
					require('@/static/detail/photo-3.jpg'),
					require('@/static/detail/photo-4.jpg'),
				],
			}
		},
		methods: {

		}
	}
</script>

<style>
	.goods .word {
		margin-top: 20rpx;
		margin-bottom: 29rpx;
	}

	.comment-data .text {
		margin: 18rpx 0;
	}

	.promotion {
		display: flex;
		align-items: center;
	}

	.sevice {
		display: flex;
	}

	.service .list {
		display: flex;
		align-items: center;
		flex-wrap: wrap;
	}

	.service .list .item {
		flex-basis: 50%;
		margin-bottom: 20rpx;
	}

	.service .list .item:last-child {
		margin-bottom: 0;
	}

	/*用户评价*/
	.user-comments .comment .user {
		display: flex;
		align-items: center;
	}

	.user-comments .comment .user .nickname {
		margin: 0 20rpx;
	}
</style>