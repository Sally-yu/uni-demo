<template>
	<view>
		<!-- <cu-custom bgColor="bg-gradual-blue" :isBack="true"><block slot="backText">返回</block><block slot="content">图标</block></cu-custom> -->

		<view class="nav-list">
			<navigator hover-class="none" :url="'/pages/basics/' + item.title" class="nav-li" navigateTo :class="'bg-'+item.color"
			 :style="[{animation: 'show ' + ((index+1)*0.2+1) + 's 1'}]" v-for="(item,index) in list" :key="index">
				<view class="nav-name">{{item.title}}</view>
			</navigator>
		</view>
		<view class="cu-tabbar-height"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				CustomBar: this.CustomBar,
				list: [{
						title: '我要发车'
					},
					{
						title: '找顺风车'
					},
					{
						title: '帮我取件'
					},
					{
						title: '发起团购'
					},
					{
						title: '找人挪车'
					},
					{
						title: '开party'
					},
					{
						title: '想要蹭饭'
					},
					{
						title: '求蹭wifi'
					},
					{
						title: '下楼约跑'
					},
					{
						title: '打赏作者'
					},
				]

			};
		},
		methods: {
			searchIcon(e) {
				let key = e.detail.value.toLowerCase();
				let list = this.cuIcon;
				for (let i = 0; i < list.length; i++) {
					let a = key;
					let b = list[i].name.toLowerCase();
					if (b.search(a) != -1) {
						list[i].isShow = true
					} else {
						list[i].isShow = false
					}
				}
				this.cuIcon = list
			}
		}
	}
</script>

<style>
	page {
		padding-top: 50px;
	}
</style>
