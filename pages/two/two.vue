<template>
	<view>
		two
    <button @click="toPath">toOne</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
    methods: {
      toPath() {
        uni.redirectTo({
          url: '../banner/banner'
        })
      }
    }
	}
</script>

<style lang="scss">

</style>
