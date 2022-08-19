<script setup lang="ts">
import Vue from 'vue'
// import CryptoJs from 'crypto'

// CryptoJs.createHash('md5').update("").digest()
</script>

<template>
    <div id="root-div" style="{ display: 'flex' }">
        <a-card id="findme-card" title="Find Me" :bordered="false">
            <a-space :size=18 >
                <a href="https://github.com/AlexZhoushaocheng" target="_blank"><img class="icon" src="../assets/github.svg" /></a>
                <a href="https://www.jianshu.com/u/cc81862dcbf7" target="_blank"><img class="icon" src="../assets/jianshu.svg" /></a>
                <a href="https://www.cnblogs.com/litesite/" target="_blank"><img class="icon" src="../assets/bokeyuan.svg" /></a>
                <a href="123" target="_blank"><img class="icon" src="../assets/juejin.svg" /></a>
            </a-space>
            <!-- <div id="icon-row" class="flex-box">
                <ul>
                    <li><img class="icon" src="../assets/github.svg" /></li>
                    <li><img class="icon" src="../assets/jianshu.svg" /></li>
                    <li><img class="icon" src="../assets/bokeyuan.svg" /></li>
                    <li><img class="icon" src="../assets/juejin.svg" /></li>
                </ul>

            </div> -->
            <a>zhoushaochengboy@foxmail.com</a>
        </a-card>
    </div>

</template>

<style scoped>
/* #icon-row {
    width: 100%;
    display: flex;
    height: 35px;
} */

.flex-box {
    display: flex;
}

.icon {
    width: 45px;
    /* height: 32px; */
}

#root-div {
    display: flex;
    justify-content: center;
    width: 100%;
    /* height: 100%; */
    /* text-align: center; */
}

#findme-card {
    width: 360px;
}
</style>