<template>
  <div :class="namespace('preview')">
    <SmartFilter style="width: 50vw" :options="options" />
  </div>
</template>

<script setup lang="ts">
import { namespace } from '@smart-filter/core'
import { SmartFilter } from '@smart-filter/vue'

const options=[
  {
    label: '名称',
    value: 'name'
  },
  {
    label: '状态',
    value: 'status'
  },
  {
    label: 'ID',
    value: 'id'
  }
]
</script>
