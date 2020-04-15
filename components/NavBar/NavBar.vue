<template>
	<view>
		navbar
    <button type="primary" @click="testChild">event</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			
			};
		},
    methods: {
      testChild() {
        // console.log('child')
        // 触发父组件的 自定义事件：handleClick
        // this.$emit("handleClick")
        
        uni.$emit('testEmit', {name: 'pop'})
      }
    }
	}
</script>

<style lang="scss" scoped>
  view {
    font-size: 16px;
  }
</style>
