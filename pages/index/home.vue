<template>
	<view class="page bg-white">
		<cu-custom bgColor="bg-yellow">
			<block slot="content">整点活吧</block>
		</cu-custom>

		<view class="bg-white padding-lg">
			<view class="nav-list ">
				<navigator hover-class="none" class="nav-li" :class="'bg-'+item.color" :url="'/pages/func/'+item.name" v-for="(item,index) in elements"
				 :key="index">
					<view class="nav-title">{{item.title}}</view>
					<!-- <view class="nav-name"></view> -->
					<text :class="'cuIcon-' + item.cuIcon"></text>
				</navigator>
			</view>
			<view class="cu-tabbar-height"></view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "basics",
		data() {
			return {
				CustomBar: this.CustomBar,
				elements: [{
						title: '我要发车',
						name: 'fache',
						color: 'cyan',
						cuIcon: 'newsfill'
					},
					{
						title: '搭顺风车',
						name: 'dache',
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
</style>
