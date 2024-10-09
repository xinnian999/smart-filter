<template>
  <svg
    t="1706682823369"
    viewBox="0 0 1024 1024"
    version="1.1"
    xmlns="http://www.w3.org/2000/svg"
    p-id="3946"
    v-html="(icons as Record<string, any>)[name]"
    :class="namespace('icon')"
  ></svg>
</template>

<script setup lang="ts">
import { icons, namespace } from '@smart-filter/core'

defineProps<{
  name: string
}>()
</script>
