<template>
	<view class="container">
		<view class="user-info">
			<view>
				<image class="avatar" :src="avatar" mode="scaleToFill" style="width: 60px;height: 60px;"></image>
				<text class="nickname" @click="login">{{ nickname }}</text>
			</view>
		</view>
		<view class="user-config">
			<uni-list class="config config-1">
				<uni-list-item title="打赏" note="开发不易,咖啡支持？" clickable @click="donation" thumb="../../static/img/icon/mine/coffee.png"
				 thumbSize="base"></uni-list-item>
				<uni-list-item title="备份或恢复数据" note="" thumb="../../static/img/icon/mine/cloud.png" thumbSize="base"></uni-list-item>
			</uni-list>
			<uni-list class="config config-2">
				<uni-list-item title="专注及时核心设置" note="铃声震动 | 自定义格言 | 休息时长" thumb="../../static/img/icon/mine/clock.png" thumbSize="base"></uni-list-item>
				<uni-list-item title="海报背景和外观设置" note="番茄钟海报 | 待办卡片背景 | 计时器外观" thumb="../../static/img/icon/mine/image.png"
				 thumbSize="base"></uni-list-item>
				<uni-list-item title="配置主界面底栏" note="选择要在主界面展示的功能模块" thumb="../../static/img/icon/mine/tool.png" thumbSize="base"></uni-list-item>
				<uni-list-item title="主题颜色搭配设置" note="主题色 | 专注分布图配色" thumb="../../static/img/icon/mine/wind.png" thumbSize="base"
				 :show-extra-icon="true" :extra-icon="extraIcon" :show-switch="true" @switchChange="switchChange"></uni-list-item>
				<uni-list-item title="其他设置" note="语言设置等" thumb="../../static/img/icon/mine/settings.png" thumbSize="base"></uni-list-item>
			</uni-list>
			<uni-list class="config config-3">
				<uni-list-item title="帮助 | 常见问题" note="常见的使用问题和解决方案" thumb="../../static/img/icon/mine/help.png" thumbSize="base"></uni-list-item>
				<uni-list-item title="分享给朋友们" note="" thumb="../../static/img/icon/mine/share.png" thumbSize="base"></uni-list-item>
			</uni-list>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				nickname: "未登录",
				avatar: "../../static/avatar.png"
			}
		},
		methods: {
			login(e) {
				console.log(this);
			},
			donation(e) {
				uni.showToast({
					title: '捐助了亿杯咖啡'
				});
			},
			switchChange(e) {
				uni.showToast({
					title: 'Switch to ' + e.value
				});

			}
		}
	}
</script>

<style scoped>
	.container {
		background-color: #f5f5f5
	}

	.user-info {
		padding: 10px;
		background-image: url('~@/static/wallpaper.jpg');
		background-size: 100% auto;
	}

	.user-info .avatar {
		border-radius: 30px;
	}

	.user-info .nickname {
		position: relative;
		top: -25px;
		left: 15px;
		color: #e3e3e3;
	}

	.user-config .config {
		margin-bottom: 5px;
	}
</style>
