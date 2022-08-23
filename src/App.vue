<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'
import Home from './components/Home.vue'
import Contact from './components/Contact.vue'
import Music from './components/Music.vue'
import Bg from './components/Bg.vue'
import LoginVue from './components/Login.vue'

import { IconCamera, IconEdit, IconUser } from '@arco-design/web-vue/es/icon';

enum ePage {
  HOME = 'HOME',
  MUSIC = 'MUSIC',
  BLOG = 'BLOG',
  CONTACT = 'CONTACT'
}

const page = ref(ePage.HOME)

const login = ref(false)
const login_form_show = ref(false)

function avatar_click(){
  // 如果一登录就直接返回
  if(login.value) return

  // 显示登录框
  login_form_show.value = !login_form_show.value
}

function user_icon_click(){
  // console.log('234')
}
</script>

<template>
  <div id="bg_img" class="bg">
    <a-menu mode="horizontal" :default-selected-keys="['1']" theme="dark" >
      <a-menu-item key="1" @click="page = ePage.HOME">HOME</a-menu-item>
      <a-menu-item key="2" @click="page = ePage.MUSIC">MUSIC</a-menu-item>
      <a-menu-item key="3" @click="page = ePage.BLOG">BLOG</a-menu-item>
      <a-menu-item key="4" @click="page = ePage.CONTACT">CONTACT</a-menu-item>
    </a-menu>
    <div id="login_avatar">
      <a-avatar :trigger-icon-style="{ color: '#3491FA' }" :auto-fix-font-size="false"
        :style="{ backgroundColor: '#168CFF' }" @click="avatar_click">
        周
        <template #trigger-icon>
          <IconUser @click="user_icon_click"/>
        </template>
      </a-avatar>
    </div>
    <Home v-if="page == ePage.HOME"> </Home>
    <Music v-if="page == ePage.MUSIC"></Music>
    <Contact v-if="page == ePage.CONTACT"></Contact>


  </div>
  <div id="brid-bg">
   <Bg></Bg>
  </div>

  <LoginVue v-if="login_form_show"></LoginVue>
  <!-- <HelloWorld msg="Vite + Vue" /> -->

</template>

<style scoped>
/* .logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
} */
/* .bg{
  height: 100%;
} */

#brid-bg{
  height: 50vh;
  width: 100VW;
  overflow:hidden; /*clip 或者hidden*/
  position:absolute;
  top: 25vh;
  z-index: 10;
  /* display: flex;   */
  /* background-color: red; */
}

#login_avatar {
  text-align: right;
  margin-top: 5px;
  padding-right: 20px;
}

#bg_img {
  z-index: -1;
  /* position: relative; */
  /* overflow: hidden; */
  /* display: flex; */
  /* align-items: center; */
  /* justify-content: center; */

  height:100vh;
  background-image: url(./assets/bg1.jpg);
  background-size: cover;
  background-position: center center;
  /* padding: 2rem; */
  /* padding-bottom: 50%; */
}

.menu-demo {
  box-sizing: border-box;
  width: 100%;
  padding: 40px;
  background-color: var(--color-neutral-2);
}
</style>

