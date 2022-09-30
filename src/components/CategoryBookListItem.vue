<script setup lang="ts">
import { defineProps } from "vue";
import { BookItem } from "@/types";
const props = defineProps<{
  book: BookItem;
}>();
const bookImageFileName = function (book: BookItem): string {
  let name = book.title.toLowerCase();
  name = name.replace(/ /g, "-");
  name = name.replace(/'/g, "");
  return `${name}.gif`;
};
</script>
<style scoped>
#book-boxes {
  display: flex;
  flex-wrap: wrap;
  padding: 1em;
  gap: 1em;
  justify-content: left;
  width: 1200px;
}

#book-image {
  display: inline-block;
}

#book-description {
  display: inline-block;
  position: relative;
  bottom: 120px;
  padding-left: 10px;
}

.book-box {
  display: inline-flex;
  flex-direction: column;
  background-color: var(--primary-color-dark);
  padding: 1em;
  gap: 0.25em;
  font-size: 22px;
}

.book-title {
  font-weight: bold;
}

.add-button {
  display: inline-block;
  background: var(--primary-color);
  color: white;
  padding: 0.5em 0.5em;
  cursor: pointer;
  border: 2px none;
  border-radius: 10px;
  margin-top: 1px;
  position: relative;
  font-size: 18px;
  top: 100px;
}

.read-button {
  display: inline-block;
  background: var(--primary-color-dark);
  color: white;
  padding: 0.5em 0.5em;
  cursor: pointer;
  border: 2px none;
  border-radius: 10px;
  margin-top: 1px;
  position: relative;
  top: 80px;
  font-size: 18px;
  opacity: 0.85;
}
.read-button,
.read-button:visited {
  display: inline-block;
  background: var(--primary-color-dark);
  color: #000000;
  text-decoration: none;
  padding: 0.5em 0.5em;
  cursor: pointer;
  border: 2px none;
  border-radius: 0px;
  opacity: 0.85;
}

.read-button:hover,
.read-button:active {
  background: var(--primary-color-dark);
  color: gray;
  opacity: 0.85;
}

.add-button,
.add-button:visited {
  display: inline-block;
  background: var(--primary-color);
  color: #000000;
  text-decoration: none;
  padding: 0.5em 0.5em;
  cursor: pointer;
  border: 2px none;
  border-radius: 0px;
}

.add-button:hover,
.add-button:active {
  background: var(--primary-color-dark);
  color: #000000;
}

.book-author {
  font-style: italic;
  position: relative;
  top: 30px;
  color: #000000;
  font-size: 20px;
}

.book-title {
  position: relative;
  color: #000000;
  top: 20px;
}

.book-price {
  position: relative;
  top: 60px;
  color: #000000;
}
</style>

<template>
  <li class="book-box">
    <div class="book-boxes">
      <div id="book-image" style="position: relative">
        <img
          :src="require('@/assets/updateImage/books/' + book.bookId + '.jpg')"
          :alt="book.title"
          width="160"
          height="auto"
        />
        <div
          style="position: absolute; left: 30px; top: 100px"
          v-if="book.isPublic === true"
        >
          <button class="read-button">Read Now</button>
        </div>
      </div>
      <div id="book-description">
        <div class="book-title" style="white-space: pre-wrap">
          {{ book.title }}
        </div>
        <div class="book-author" style="white-space: pre-wrap">
          {{ book.author }}
        </div>
        <div class="book-price">${{ (book.price / 100).toFixed(2) }}</div>
        <button class="add-button">
          <font-awesome-icon icon="fa-solid fa-cart-shopping" />
          Add to Cart
        </button>
      </div>
      <!--    <button class="button">Read Now</button>-->
    </div>
  </li>
</template>
