<template>
  <div :class="namespace('container')">
    <input type="text" v-model="q" />
  </div>
</template>

<script setup lang="ts">
import { namespace } from '@smart-filter/core';
import { ref } from 'vue'

const q = ref('')
</script>
