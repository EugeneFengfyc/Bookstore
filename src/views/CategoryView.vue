<script setup lang="ts">
import { provide } from "vue";
import { BookItem } from "@/types";
import CategoryNav from "@/components/CategoryNav.vue";
import CategoryBookList from "@/components/CategoryBookList.vue";
const bookList: BookItem[] = [
  {
    bookId: 1001,
    title: "Violeta",
    author: "Isabel Allende",
    price: 2604,
    isPublic: true,
  },
  {
    bookId: 1002,
    title: "The Marriage\n" + "Portrait",
    author: "Maggie O'Farrell",
    price: 2904,
    isPublic: false,
  },
  {
    bookId: 1003,
    title: "Smart Brevity",
    author: "Mike Allen",
    price: 2511,
    isPublic: true,
  },
  {
    bookId: 1004,
    title: "Be Not Afraid\n" + "of Love",
    author: "Mimi Zhu",
    price: 699,
    isPublic: false,
  },
  {
    bookId: 1005,
    title: "Utopia",
    author: "J. Bradford\n" + "DeLong",
    price: 3500,
    isPublic: false,
  },
  {
    bookId: 1006,
    title: "What We Owe\n" + "the Future",
    author: "William\n" + "Macaskill",
    price: 2976,
    isPublic: false,
  },
];
//provide("bookList", bookList);
</script>

<style scoped></style>

<template>
  <div>
    <category-nav></category-nav>
    <category-book-list :bookList="bookList"> </category-book-list>
  </div>
</template>
