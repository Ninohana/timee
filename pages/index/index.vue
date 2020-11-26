<template>
	<view class="container">
		<view class="body" v-for="d in data">
			<uni-card @click="onClick" title="锻炼" mode="title" thumbnail="" extra="30min" note="停掉手头上的工作,享受锻炼带来的乐趣" thumbnail="https://img-cdn-qiniu.dcloud.net.cn/new-page/uni.png">
				{{ d }}:跑步、篮球、乒乓……
			</uni-card>
		</view>
	</view>
</template>

<script>
	import uCard from '../../components/uni-card/uni-card.vue'

	export default {
		comments: {
			uCard
		},
		data() {
			return {
				data: [1, 2]
			}
		},
		methods: {
			onClick(e) {
				uni.hideToast();
				uni.showToast({
					title: "已完成"
				});
			}
		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
