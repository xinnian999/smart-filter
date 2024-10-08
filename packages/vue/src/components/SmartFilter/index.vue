<template>
  <div>
    <input type="text" v-model="q" />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const q = ref('')
</script>
