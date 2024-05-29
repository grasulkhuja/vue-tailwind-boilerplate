<script setup>
import { computed, inject } from 'vue'

const accordionButtonId = inject('accordionButtonId')

const accordionContentId = inject('accordionContentId')

const expandedItems = inject('expandedItems')

const accordionItemExpanded = computed(() => {
  return expandedItems.value.includes(accordionContentId.value)
})
</script>

<template>
  <div
    :id="accordionContentId"
    role="region"
    :aria-labelledby="accordionButtonId"
    :class="{
      'hidden': !accordionItemExpanded
    }"
    class="accordion-content"
  >
    <slot />
  </div>
</template>

<style scoped>

</style>
