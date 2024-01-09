<script setup lang="ts">
import SectionAccordion from "./SectionAccordion.vue";
import SectionTab from "./SectionTab.vue";

</script>

<template>
  <div class="md:hidden">
    <SectionAccordion/>
  </div>
  <div class="hidden md:block">
    <SectionTab/>
  </div>
</template>
