<script setup lang="ts">
import ref from 'vue'

import TimelineItemVue from './TimelineItem.vue';
import LovelyGhostVue from './LovelyGhost.vue';

import { IconFire } from '@arco-design/web-vue/es/icon';

import img_bitcoin from '/src/assets/bitcoin.png'
import img_cloud from '/src/assets/cloud.svg'
import img_home from '/src/assets/home.svg'

// const coin = new URL('../assets/bitcoin.png', import.meta.url).href
</script>

<template>
  <div id="root-left">
    <div id="text">
      <h1>Hi~</h1>
      <p>我是一个 <span class="cpp">c++</span>程序员，这里是我的闲暇涂鸦。旨在自我娱乐和学习，没有什么对外服务哦。如果你是无意间发现了这里，那么也很高兴认识你~😘</p>

      <p>我嘛~ 就喜欢瞎折腾 🥂</p>

      <p>这里？</p>
    </div>
    <!-- <img src="../assets/bitcoin.png"> -->
    <div id="timeline-div">
      <div>
        <a-timeline direction="horizontal" mode="alternate" label-position="relative" pending="">
        <template #dot>
          <IconFire :style="{ color: '#e70a0a' }" />
        </template>
        <a-timeline-item label="有一天" dotColor="#F53F3F">
          <TimelineItemVue :img_url="img_bitcoin" title="NAS主机" desc="买了个矿渣弄个私有云"></TimelineItemVue>
        </a-timeline-item>
        <a-timeline-item label="后来" dotColor="#00B42A">
          <TimelineItemVue label_="后来" :img_url="img_cloud" title="域名" desc="可公网访问私有云了"></TimelineItemVue>
        </a-timeline-item>
        <a-timeline-item label="然后">
          <TimelineItemVue label_="然后" :img_url="img_home" title="主页" desc="于是我有个了主页"></TimelineItemVue>
        </a-timeline-item>
      </a-timeline>
      </div>

    </div>
  </div>
  <div id="root-right">
   <LovelyGhostVue></LovelyGhostVue>
  </div>
</template>

<style scoped>
/* #timeline-div {
  
} */

#timeline-div>div{
  padding: 30px;
  margin: 50px 250px 50px 50px;
  background: #FFFFE070;
  border-radius: 10px;
}

.cpp {
  color: aqua;
}

#root-left,
#root-right {
  margin-top: 120px;
  width: 50%;
  height: 500px;
  float: left;
  /* display: inline-block; */

  /* display: block; */
  /* background-color: blue; */
}

#text,
#timeline-div {
  margin: 0px 10px 10px 35px;
  
  /* height: auto; */
  /* display: inline-block; */
  /* display: flex; */
  /* float: left; */
  /* background-color: red; */
}

p,
h1 {
  font-family: 微软雅黑;
  font-size: 25px;
  line-height: 30px;
  text-align: left;
}


</style>