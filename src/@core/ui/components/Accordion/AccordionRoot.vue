<script setup>
import { provide, ref } from 'vue'

const props = defineProps({
  multiple: {
    type: Boolean,
    default: false
  }
})

const expandedItems = ref([])
provide('expandedItems', expandedItems)

provide('isMultiple', props.multiple)
</script>

<template>
  <div id="accordionRoot" class="accordion-root">
    <slot />
  </div>
</template>


