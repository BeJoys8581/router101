<script setup>
import { RouterView } from 'vue-router';
import HeaderDD from './views/HeaderDD.vue';
import FooterDD from '@/views/FooterDD.vue'
</script>

<template>
<HeaderDD/>
<div class="container">
<RouterView/>
</div>
<FooterDD/>
</template>

<style scoped>

</style>
