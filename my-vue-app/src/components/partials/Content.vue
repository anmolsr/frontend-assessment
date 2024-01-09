<script setup lang="ts">
import ContentCard from "./ContentCard.vue";

const items = [
  {
    image: "https://via.placeholder.com/400x300",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque tempor, nibh id tincidunt molestie, eros metus tincidunt elit, ac egestas eros quam non est. Proin in lorem a mi finibus",
    linkTo: "https://example.com/image1",
  },
  {
    image: "https://via.placeholder.com/400x300",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque tempor, nibh id tincidunt molestie",
    linkTo: "https://example.com/image2",
  },
  {
    image: "https://via.placeholder.com/400x300",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque tempor, nibh id tincidunt molestie, eros metus tincidunt elit,",
    linkTo: "https://example.com/image3",
  },
];
</script>

<template>
  <div class="container py-6">
    <!-- <ContentCard v-for="(data, index) in contentData" :key="index" :data="data"/> -->
    <div class="space-y-4 sm:grid sm:grid-cols-2 sm:space-y-0 sm:gap-4 lg:grid-cols-3">
      <ContentCard v-for="item in items" :key="item.id" :data="item" />
    </div>
  </div>
</template>
