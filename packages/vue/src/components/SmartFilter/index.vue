<template>
  <div :class="namespace('container')">
    <input
      :class="namespace('inner')"
      type="text"
      v-model="q"
      placeholder="多个关键字用竖线 “|” 分隔，多个过滤标签用回车键分隔"
    />
    <Icon name="search" />
  </div>
</template>

<script setup lang="ts">
import { namespace } from '@smart-filter/core'
import { Icon } from '@smart-filter/vue'
import { ref } from 'vue'

const q = ref('')
</script>
