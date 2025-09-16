<script setup>
import { RouterLink } from "vue-router";

const props = defineProps({
  image: String,
  title: String,
  subTitle: String,
});
</script>

<template>
  <RouterLink to="library">
    <div
      class="bg-[111111] p-4 rounded-md m-2 hover:bg-[#252525] cursor-pointer"
    >
      <img class="rounded-md" :src="props.image" />
      <div class="text-white pt-4 font-semibold text-[17px]">{{ title }}</div>
      <div class="text-gray-400 pt-1 pb-3 text-[14px]">{{ subTitle }}</div>
    </div>
  </RouterLink>
</template>
