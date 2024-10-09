<template>
  <img :src="(icons as Record<string,any>)[name]" :class="namespace('icon')" />
</template>

<script setup lang="ts">
import { icons, namespace } from '@smart-filter/core'

defineProps<{
  name: string
}>()
</script>
