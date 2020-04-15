<template>
	<view class="content">
    <nav-bar :name="name" @handleClick="testEvent"></nav-bar>
	</view>
</template>

<script>
  import NavBar from '../../components/NavBar/NavBar.vue'
	export default {
		data() {
			return {
				title: 'Hello',
        name: 'allen'
			}
		},
    components: {
      NavBar
    },
		onLoad() {
      // 事件订阅
      // 可以重复触发
      uni.$on('testEmit',(arg) => {
        console.log(arg)
      })
      // 只能触发一次
      uni.$once('testEmit',(arg) => {
        console.log(arg, '我只能触发一次')
      })
		},
		methods: {
      testEvent() {
        // console.log('parents')
      }
		}
	}
</script>

<style>
</style>
