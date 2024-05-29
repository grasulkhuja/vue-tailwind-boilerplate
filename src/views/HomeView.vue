<script setup>
import AccordionRoot from '@/@core/ui/components/Accordion/AccordionRoot.vue'
import AccordionItem from '@/@core/ui/components/Accordion/AccordionItem.vue'
import AccordionItemTitle from '@/@core/ui/components/Accordion/AccordionItemTitle.vue'
import AccordionItemContent from '@/@core/ui/components/Accordion/AccordionItemContent.vue'


</script>

<template>
  <main class="flex w-full h-full justify-center items-center min-h-full">
    <AccordionRoot>
      <AccordionItem>
        <AccordionItemTitle>title</AccordionItemTitle>
        <AccordionItemContent>content</AccordionItemContent>
      </AccordionItem>
      <AccordionItem>
        <AccordionItemTitle>title1</AccordionItemTitle>
        <AccordionItemContent>content1</AccordionItemContent>
      </AccordionItem>
    </AccordionRoot>
  </main>
</template>
