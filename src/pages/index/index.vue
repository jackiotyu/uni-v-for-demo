<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view>
			<text class="title">{{title}}</text>
		</view>

		<view v-for="item in list" :key="item.id" :data-name="mapName(item)">
			{{ item.name }}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				list: [
					{
						id: 1,
						name: 'a'
					},
					{
						id: 2,
						name: 'b'
					},
					{
						id: 3,
						name: 'c'
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			mapName(item) {
				return 'u-' + item.name
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin: 200rpx auto 50rpx auto;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
