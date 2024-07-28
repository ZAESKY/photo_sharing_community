<template>
  <van-nav-bar>
    <template #left>
    <van-image
  round
  width="50rpx"
  height="50rpx"
  src="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg"
/>
  </template>
  <template #right>
    <van-icon name="chat-o" dot size="20" style="margin-right:35rpx;"/>
    <van-button type="primary" size="mini" plain icon="plus" round>发布</van-button>
  </template>
</van-nav-bar>
<van-search v-model="value" placeholder="请输入搜索关键词" shape='round'/>
<van-tabs v-model:active="active" sticky animated>
  <van-tab v-for="index in 2" :title="'标签 ' + index">
    <van-grid :border="false" :column-num="2">
  <van-grid-item>
    <van-image
      src="https://fastly.jsdelivr.net/npm/@vant/assets/apple-1.jpeg"
    />
  </van-grid-item>
  <van-grid-item>
    <van-image
      src="https://fastly.jsdelivr.net/npm/@vant/assets/apple-2.jpeg"
    />
  </van-grid-item>
  <van-grid-item>
    <van-image
      src="https://fastly.jsdelivr.net/npm/@vant/assets/apple-3.jpeg"
    />
  </van-grid-item>
</van-grid>
  </van-tab>
</van-tabs>

</template>

<script setup>
import { ref } from "vue";

  const title = ref('hello')
  const jump = () => {
    uni.navigateTo({
       url: '/pages/login/login'
    });
  }
</script>

<style scoped>
::v-deep .van-nav-bar__title{
  width: 75% !important;
  max-width: unset;
}
</style>
