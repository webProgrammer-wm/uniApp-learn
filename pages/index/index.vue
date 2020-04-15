<template>
	<view class="content">
    <nav-bar></nav-bar>
    <text>首页</text>
    {{ 'hello' }}
    <view> {{ name }}</view>
    <view>{{ 'hello' + name }}</view>
    <view>{{ 'allen'.indexOf('a') ? 'web' : '???' }}</view>
    <view>{{ '我爱中国'.slice(0, 1) }}</view>
    <view>{{ false || '' || '你想看什么' }}</view>
    <img :src="imgUrl" />
    
    <!-- 小程序写法，编辑器会报错，但能产生实际效果 -->
    <!-- <view class="box{{1}}">test</view> -->
    <view :class="'box' + 111"></view>
    <view :style="{ width:'100px', height:'100px',background:'pink'}"></view>
    
    <view v-for="(item, index) in names" 
          :key="index"
          :class="{ box2: index === curIndex  }"
          @click="setIndex(index)"
    >
      {{ item }}
    </view>
    
    <button type="primary" @click="toPath">toNews</button>
	</view>
</template>

<script>
  import NavBar from '../../components/NavBar/NavBar.vue'
	export default {
		data() {
			return {
        name: 'allen',
        imgUrl: 'https://dss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=2235388275,3809603206&fm=85&app=79&f=JPG?w=121&h=75&s=8197C732C535FA313E526557030030BB',
        names: ['alex', 'allen', 'bluce'],
        curIndex: 0
      }
		},
    components: {
      NavBar
    },
		onLoad() {
		},
		methods: {
      setIndex(index) {
        this.curIndex = index
      },
      toPath() {
        // 跳转到 pages.json 配置好的页面
        // uni.switchTab({
          // url: '../news/news'
        // })
        
        // 保留当前页面 跳转到没在 pages.json 配置的页面
        uni.navigateTo({
          url: '../banner/banner?name=allen'
        })
      }  
		}
	}
</script>

<style lang="scss">
  .box1 {
    background: #000;
    width: 100px;
    height: 100px;
  }
  
  .box2 {
    background-color: pink;
  }
  
  .box3 {
    background: green;
    width: 100px;
    height: 100px;
  }
</style>
