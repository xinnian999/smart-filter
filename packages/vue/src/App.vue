<template>
  <div :class="namespace('preview')">
    <SmartFilter/>
  </div>
</template>

<script setup lang="ts">
import { namespace } from "@smart-filter/core";
import SmartFilter from './components/SmartFilter/index.vue'
</script>
