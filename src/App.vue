<script setup lang="ts">
import { provide } from "vue";
import { CategoryItem } from "@/types";
import AppHeader from "@/components/AppHeader.vue";
import AppFooter from "@/components/AppFooter.vue";
const categoryList: CategoryItem[] = [
  { categoryId: 1001, name: "Best Sellers" },
  { categoryId: 1002, name: "Literature" },
  { categoryId: 1003, name: "Science" },
  { categoryId: 1004, name: "Art" },
  { categoryId: 1005, name: "Health" },
  { categoryId: 1006, name: "Cook" },
  { categoryId: 1007, name: "Comics" },
  { categoryId: 1008, name: "Magazine" },
];
provide("categoryList", categoryList);
</script>

<style></style>

<template>
  <div id="app">
    <app-header></app-header>
    <router-view></router-view>
    <app-footer></app-footer>
  </div>
</template>
