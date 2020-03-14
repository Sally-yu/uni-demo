<template>
	<view>
		<view class="cu-bar bg-white fixed search padding" :style="[{top:CustomBar + 'px'}]">
			<view class="text-xl">今日收入</view>
			<view class="text-xl"><text :class="sum>0?'text-red':'text-green'">{{sum}}</text></view>
		</view>
		<view class="cu-bar bg-white ">
		</view>
		<view class="cu-timeline padding">
			<view class="cu-time">今天</view>
			<view v-for="(item,index) in list" :key="index" class="cu-item" :class="item.type==1?'text-red':''">
				<view class="align-end text-grey">10:09</view>
				<view v-if="item.type==0" class="content shadow-blur ">
					<view>{{item.title}}</view>
					<view>-{{item.amount}}</view>
				</view>
				<view v-if="item.type==1" class="content bg-red shadow-blur justify-between">
					<view>{{item.title}}</view>
					<view>{{item.amount}}</view>
				</view>
			</view>
		</view>
		<view class="cu-load bg-gray over"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						type: 1,
						amount: 0,
						time: 1584155248,
						title: '灰色收入'
					},
					{
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '地铁'
					},
					{
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '买菜'
					},
					{
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '外卖'
					},
					{
						type: 1,
						amount: 0,
						time: 1584155248,
						title: '红包'
					},
					{
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '捡到钱'
					}, {
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '地铁'
					},
					{
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '买菜'
					},
					{
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '外卖'
					},
					{
						type: 1,
						amount: 0,
						time: 1584155248,
						title: '红包'
					},
					{
						type: 0,
						amount: 0,
						time: 1584155248,
						title: '捡到钱'
					},
				],
				sumIn: 0,
				sumOut: 0,
				sum: 0
			}
		},
		methods: {
			calcSum() {
				this.list.forEach(a => {
					let num = 40.08;
					a.amount = num;
					if (a.type == 0) {
						this.sumOut += num
					} else {
						this.sumIn += num;
					}
				});
				this.sum = Math.floor((this.sumIn - this.sumOut) * 100) / 100;
			},
			getList(){
				
			}
		},
		onShow() {
			this.calcSum();
		},
		onPullDownRefresh() {

		}
	}
</script>

<style>

</style>
