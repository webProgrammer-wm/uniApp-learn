<template>
	<view>
		<view v-show="false">v-show</view>
    <view v-if="false">v-if</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view>
    <view>xxx</view><view>xxx</view>
    <view>xxx</view>
    
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
    onLoad() {
      // 进入此页面初触发
      console.log('页面初始化 执行一次 onload')
    },
    onReady() {
      // 此页面加载完成的时候触发
      console.log('页面加载完成 执行一次 onReady')
    },
    onShow() {
      // 显示此页面的时候触发
      console.log('页面进入执行 执行多次 onShow')
    },
    onHide() {
      // 离开了此页面触发
      console.log('页面进入离开 执行多次 onHide')
    },
    onPullDownRefresh() {
      console.log('用户执行了下拉加载动作')
    },
    // 页面滚动到底部触发
    onReachBottom() {
      console.log('你已经到底了')
    },
    // 切换到该页面时触发
    onTabItemTap() {
      console.log('欢迎收看新闻')
    },
    // 用户触发分享
    onShareAppMessage() {
      console.log('用户进行了分享')
      return {
        title: "自定义的分享标题",
        path: '/pages/news/news',
        imageUrl: '/static/logo.png' 
      }
    },
    // 参数是滚动条距离顶部的像素值
    onPageScroll(obj) {
      console.log(obj)
    },
		methods: {
			
		}
	}
</script>

<style>

</style>
