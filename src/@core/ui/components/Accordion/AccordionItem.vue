<script setup>
import { provide, ref } from 'vue'
import { genUUID } from '@/@core/composables/genUUID.js'

const accordionButtonId = ref(genUUID())
provide('accordionButtonId', accordionButtonId)

const accordionContentId = ref(genUUID())
provide('accordionContentId', accordionContentId)

</script>

<template>
  <div id="accordionItem" class="accordion-item">
    <slot />
  </div>
</template>

