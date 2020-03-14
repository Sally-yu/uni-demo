<template>
	<view class="bg-white">
		<view class="cu-bar "></view>
		<view class="nav-list ">
			<navigator hover-class="none"  class="nav-li"  :class="'bg-'+item.color"
			 v-for="(item,index) in elements" :key="index">
				<view class="nav-title">{{item.title}}</view>
				<view class="nav-name">{{item.name}}</view>
				<text :class="'cuIcon-' + item.cuIcon"></text>
			</navigator>
		</view>
		<view class="cu-tabbar-height"></view>
	</view>
</template>

<script>
	export default {
		name: "basics",
		data() {
			return {
				elements: [{
						title: '我要发车',
						name: 'layout',
						color: 'cyan',
						cuIcon: 'newsfill'
					},
					{
						title: '搭顺风车',
						name: 'background',
						color: 'blue',
						cuIcon: 'colorlens'
					},
					{
						title: '发起团购',
						name: 'text',
						color: 'purple',
						cuIcon: 'font'
					},
					{
						title: '开Party ',
						name: 'icon',
						color: 'mauve',
						cuIcon: 'cuIcon'
					},
					{
						title: '找人挪车',
						name: 'button',
						color: 'pink',
						cuIcon: 'btn'
					},
					{
						title: '想蹭个饭',
						name: 'tag',
						color: 'brown',
						cuIcon: 'tagfill'
					},
					{
						title: '楼下约跑',
						name: 'avatar',
						color: 'red',
						cuIcon: 'myfill'
					},
					{
						title: '来打牌啊',
						name: 'progress',
						color: 'orange',
						cuIcon: 'icloading'
					},
					{
						title: '我要吐槽',
						name: 'shadow',
						color: 'olive',
						cuIcon: 'copy'
					},
					{
						title: '打赏作者',
						name: 'loading',
						color: 'green',
						cuIcon: 'loading2'
					}
				],
			};
		},
		onShow() {
			console.log("success")
		}
	}
</script>

<style>
	.page {
		height: 100vh;
	}
</style>
