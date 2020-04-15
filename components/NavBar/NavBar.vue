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
    beforeMount() {
      console.log('在挂载开始之前被调用')
    },
    mounted() {
      console.log('挂载到实例上去之后调用')
      this.$nextTick(function(){
        // 渲染完毕
        console.log('ok')
      })
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
