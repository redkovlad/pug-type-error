<script setup lang="ts">
import '../assets/css/counterStyle.css'
import { usePiniaStore } from '@/stores/piniaStore';

const store = usePiniaStore();

setInterval(() => store.increment(), 1000);
</script>
<template>
    <div class="counter">{{ store.count }}</div>
</template>