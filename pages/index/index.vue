<template>
	<view>
		<view class="Mainname">
			<u--text text="病" size="50rpx" color="#333" align="center"></u--text>
			<u--text text="虫" size="50rpx" color="#333" align="center"></u--text>
			<u--text text="害" size="50rpx" color="#333" align="center"></u--text>
			<u--text text="名" size="50rpx" color="#333" align="center"></u--text>
			<u--text text="称" size="50rpx" color="#333" align="center"></u--text>
			<u-line length="900rpx" margin="10rpx 0"></u-line>
		</view>
		<u-grid :border="true" col="2">
			<u-grid-item v-for="(listItem,listIndex) in list" :key="listIndex">
				<text class="grid-name">{{listItem.name}}</text>
				<text class="grid-word">{{listItem.word}}</text>
			</u-grid-item>
		</u-grid>
		<u-line length="900rpx" margin="6rpx 0"></u-line>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						name: '病虫害症状',
						word: '~~'
					},
					{
						name: '防治方法',
						word: '~~'
					},
					{
						name: '分布区域',
						word: '~~'
					},
					{
						name: '危害作物',
						word: '~~'
					},
				],
			}
		},

	}
</script>

<style lang="scss">
	.grid-name {
		font-size: 50px;
		color: #909399;
		padding: 5rpx 20rpx 20rpx 0rpx;
		box-sizing: border-box;
	}

	.grid-word {
		font-size: 50px;
		color: #909399;
		padding: 5rpx 20rpx 20rpx 0rpx;
		box-sizing: border-box;
	}
</style>