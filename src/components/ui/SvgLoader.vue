<script lang="ts" setup>
import { computed, defineAsyncComponent, type Component } from 'vue'

const props = defineProps<{ name: string }>()

const svgs = import.meta.glob<() => Promise<{ default: Component }>>('../../assets/svg/**/*.svg')

const icon = computed(() => {
  const loader = svgs[`../../assets/svg/${props.name}.svg`]

  if (!loader) {
    console.warn(`SVG not found: ${props.name}`)
    return null
  }

  return defineAsyncComponent(loader)
})
</script>

<template>
  <component v-if="icon" :is="icon" class="fill-current" />
</template>
