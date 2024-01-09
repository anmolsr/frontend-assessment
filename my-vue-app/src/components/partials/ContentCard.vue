<script setup lang="ts">
import { defineProps } from "vue";
const { data } = defineProps(["data"]);

import {
  Card,
  CardContent,
  CardFooter,
  CardHeader,
} from "@/components/ui/card";
import { Button } from "@/components/ui/button";
</script>

<template>
  <Card>
    <CardHeader>
      <img :src="data.image" alt="Card Image" />
    </CardHeader>
    <CardContent class="text-center">
      {{ data.description }}
    </CardContent>
    <CardFooter class="text-center">
      <Button variant="outlineAr">read more</Button>
    </CardFooter>
  </Card>
</template>
