<script setup lang="ts">
import { inject } from "vue";
const categoryList = inject("categoryList");
</script>

<style scoped>
.category-buttons {
  display: flex;
  flex-direction: row;
  text-align: center;
  background-color: var(--primary-background-color);
  width: 1200px;
  font-size: 25px;
}

.button.selected-category-button {
  background-color: var(--primary-color-dark);
}

.button.unselected-category-button,
.button.unselected-category-button:visited {
  background-color: var(--primary-color);
}

.button.unselected-category-button:hover,
.button.unselected-category-button:active {
  background-color: var(--primary-color-dark);
}
.category-book-list {
  width: 1200px;
  background-color: #ffffff;
  text-align: center;
}
</style>

<template>
  <nav class="category-nav">
    <ul class="category-buttons">
      <li v-for="category in categoryList" :key="category.categoryId">
        <router-link
          :to="'../category/' + category.name"
          class="button unselected-category-button"
        >
          {{ category.name }}
        </router-link>
      </li>
    </ul>
  </nav>
</template>
