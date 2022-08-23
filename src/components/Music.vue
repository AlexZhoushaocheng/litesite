<script setup lang="ts">
    import {getCurrentInstance, onMounted, ref} from "vue";
    import Dancer from './Dancer.vue'

    function loop(){
        console.log(player.value)
    }
    const player = ref<HTMLAudioElement>();
    
</script>

<template>
    <div>
        <!-- <Dancer></Dancer> -->
        <!-- <button @click="loop"></button> -->
        <audio ref='player' id="music" loop="true" autoplay src="https://web.opendrive.com/api/v1/download/file.json/OV84MDUyNTM1NF9aSXB6Sw?inline=1"></audio>
    </div>
</template>

<style lang="scss" scoped>

</style>