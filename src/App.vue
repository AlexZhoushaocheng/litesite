<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div id="bg_img" class="bg">
    <a-menu mode="horizontal" :default-selected-keys="['1']" theme="dark">
      <!-- <a-menu-item key="0" :style="{ padding: 0, marginRight: '38px' }" disabled>
        <div
          :style="{
            width: '80px',
            height: '30px',
            borderRadius: '2px',
            background: 'var(--color-fill-3)',
            cursor: 'text',
          }"
        ></div>
      </a-menu-item> -->
      <a-menu-item key="1">HOME</a-menu-item>
      <a-menu-item key="2">MUSIC</a-menu-item>
      <a-menu-item key="3">BLOG</a-menu-item>
      <a-menu-item key="4">CONTACT</a-menu-item>
    </a-menu>
  </div>
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

#bg_img{
  /* margin: 0; */
  height: 100%;
  background-image: url(./assets/bg1.jpg);
  background-size: cover;
  /* padding-bottom: 50%; */
}

.menu-demo {
  box-sizing: border-box;
  width: 100%;
  padding: 40px;
  background-color: var(--color-neutral-2);
}
</style>
