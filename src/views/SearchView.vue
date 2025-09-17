<script setup>
import { ref } from "vue";
import categoriesData from "../assets/Categories_Data.json";
import CategorySelect from "../components/CategorySelect.vue";

const categories = ref(categoriesData);
</script>

<template>
  <div class="p-8">
    <button
      type="button"
      class="text-white text-2xl font-semibold hover:underline cursor-pointer"
    >
      Podcast to make you smarter
    </button>
    <div class="py-1.5"></div>
    <div
      class="grid xl:grid-cols-5 lg:grid-cols-4 md:grid-cols-3 sm: grid-cols-2 gap-6"
    >
      <CategorySelect
        v-for="(item, index) in categories"
        :key="index"
        :category="item.category"
        :image="item.image"
      />
    </div>
  </div>
</template>
