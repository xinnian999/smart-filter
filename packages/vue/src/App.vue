<template>
  <div :class="namespace('preview')">
    <SmartFilter style="width: 50vw" />
  </div>
</template>

<script setup lang="ts">
import { namespace } from '@smart-filter/core'
import { SmartFilter } from '@smart-filter/vue'
</script>
