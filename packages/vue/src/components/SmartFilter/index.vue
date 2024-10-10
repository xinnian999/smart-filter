<template>
  <div :class="namespace('container')">
    <div :class="namespace('inner')">
      <input
        :class="namespace('inner-input')"
        type="text"
        v-model="q"
        placeholder="多个关键字用竖线 “|” 分隔，多个过滤标签用回车键分隔"
        @focus="onFocus"
        @blur="onBlur"
      @keydown.enter="handleSearch"
        ref="inputRef"
      />

      <ul v-if="visible" :class="namespace('inner-dropdown')">
        <p :class="namespace('inner-dropdown-title')">请选择过滤类型</p>
        <li
          :class="namespace('inner-dropdown-item')"
          v-for="{ label, value } in options"
          :key="value"
          @click="handleSelect(value)"
        >
          {{ label }}
        </li>
      </ul>
    </div>

    <Icon name="search" />
  </div>
</template>

<script setup lang="ts">
import { namespace } from '@smart-filter/core'
import { Icon } from '@smart-filter/vue'
import { ref } from 'vue'

const props = defineProps<{
  options: { label: string; value: string }[]
}>()

const inputRef = ref()

const q = ref('')

const visible = ref(false)

const onFocus = () => {
  if (q.value) return
  visible.value = true
}

const onBlur = () => {
  // visible.value = false
}

const handleSelect = (value: string) => {
  const source = props.options.find((item) => item.value === value)!

  q.value = `${source.label}:`

  visible.value = false

  inputRef.value.focus()
}

const handleSearch=()=>{
  q.value=''
}
</script>
