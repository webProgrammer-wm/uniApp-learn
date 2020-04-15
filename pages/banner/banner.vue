<template>
	<view>
		one
    <button @click="toPath">toTwo</button>
    <button @click="goBack">返回</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
    onLoad(option) {
      // 获取传递的参数
      console.log(option)
    },
    methods: {
      toPath() {
        // 反复跳转页面并保留当前页面的话，只能跳有限的次数，栈满了就不能跳转了
        // uni.navigateTo({
          // url: '../two/two'
        // })
        
        // 如果在需要反复跳转页面的情况下，应该使用 uni.redirectTo
        // 关闭当前页面进行跳转
        uni.redirectTo({
          url: '../two/two'
        })
      },
      
      // 关闭当前页面，返回上一页面或多级页面。
      // 可通过 getCurrentPages() 获取当前的页面栈，决定需要返回几层。
      goBack() {
        uni.navigateBack()
      }
    }
	}
</script>

<style lang="scss">

</style>
