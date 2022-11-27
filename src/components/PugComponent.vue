<script setup lang="ts">
import '../assets/css/counterStyle.css'
import { usePiniaStore } from '@/stores/piniaStore';

const store = usePiniaStore();

setInterval(() => store.increment(), 1000);
</script>
<template lang="pug">
.counter {{ store.count }}
// Тут корректно выдаст ошибку при npm run type-check
.counter {{ store.noname }}
</template>