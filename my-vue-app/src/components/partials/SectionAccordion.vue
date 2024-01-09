<script setup lang="ts">
import {
  Accordion,
  AccordionContent,
  AccordionItem,
  AccordionTrigger,
} from "@/components/ui/accordion";
import accordionItems from '/../data.json';
const defaultValue = 'Section 1';

</script>

<template>
  <Accordion type="single" class="w-full" collapsible :default-value="defaultValue">
    <AccordionItem v-for="item in accordionItems" :key="item.title" :value="item.title">
      <AccordionTrigger class="text-lg">{{ item.title }}</AccordionTrigger>
      <AccordionContent>
        <div v-html="item.content"></div>
      </AccordionContent>
    </AccordionItem>
  </Accordion>
</template>
