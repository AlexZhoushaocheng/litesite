<script setup lang="ts">
import { ref } from 'vue'

defineProps<{img_url:string, title:string, desc:string}>();
</script>


<template>
    <!-- <a-timeline-item :label=label_> -->
        <a-row :style="{ display: 'inline-flex', alignItems: 'center' }">
            <img width="40" :style="{ marginRight: '16px', marginBottom: '12px' }"
                :src=img_url />
            <div :style="{ marginBottom: '12px' }">
                {{title}}
                <div :style="{ fontSize: '12px', color: '#4E5969' }">
                    {{desc}}
                </div>
            </div>
        </a-row>
    <!-- </a-timeline-item> -->
</template>