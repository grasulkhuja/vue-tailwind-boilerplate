<script setup>
import { computed, inject } from 'vue'

const accordionButtonId = inject('accordionButtonId')
const accordionContentId = inject('accordionContentId')
const isMultiple = inject('isMultiple')

const expandedItems = inject('expandedItems')

const accordionItemExpanded = computed(() => {
  return expandedItems.value.includes(accordionContentId.value)
})

function toggleAccordionItem() {
  const found = expandedItems.value.find(item => item === accordionContentId.value)

  if (isMultiple) {
    expandedItems.value.push(accordionContentId.value)

    return
  }

  expandedItems.value = []
  
  if (found) return

  expandedItems.value.push(accordionContentId.value)

}

</script>

<template>
  <h3 class="accordion-wrapper">
    <button
      :id="accordionButtonId"
      type="button"
      :aria-expanded="accordionItemExpanded"
      :aria-controls="accordionContentId"
      class="accordion-button"
      @click="toggleAccordionItem"
    >
      <span id="accordionItemTitle" class="accordion-title">
        <slot />
      </span>
      <span id="accordionItemIcon" class="accordion-item-icon">
        {{ accordionItemExpanded ? 'close' : 'open' }}
      </span>
    </button>
  </h3>
</template>

<style scoped>

</style>
