<script setup lang="ts">
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
import tabItems from "/../data.json";
const defaultValue = "Section 1";
</script>

<template>
  <Tabs :default-value="defaultValue" class="w-full py-4">
    <TabsList class="w-full h-full">
      <TabsTrigger
        v-for="item in tabItems"
        :key="item.title"
        :value="item.title"
      class="text-xl mx-4 p-2">
        {{ item.title }}
      </TabsTrigger>
    </TabsList>
    <TabsContent v-for="item in tabItems" :key="item.title" :value="item.title">
      <div v-html="item.content" class="w-11/12 m-auto pt-4"></div>
    </TabsContent>
  </Tabs>
</template>
