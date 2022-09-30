<script setup lang="ts">
import HeaderDropdown from "@/components/HeaderDropdown.vue";
</script>

<style scoped>
header {
  background: #ffffff;
  display: flex;
  padding: 1em;
  gap: 1em;
  justify-content: space-between;
  width: 1200px;
  height: 150px;
  font-size: 23px;
  /*color: var(--primary-color);*/
}

.text-logo {
  display: inline-block;
}

#logo-image {
  float: left;
}

#logo-text {
  float: left;
  padding: 5px;
}

.bookstore-logo {
  text-align: left;
  float: left;
  padding-left: 50px;
}

.title-and-search-bar {
  text-align: center;
  margin-top: 20px;
}

.categories-cart-login {
  text-align: right;
  margin-top: 10px;
}

.title-and-search-bar input[type="text"] {
  padding: 10px;
  font-size: 18px;
  border: 3px solid var(--primary-color-dark);
  float: left;
  width: 80%;
  background: #f1f1f1;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
.title-and-search-bar button {
  float: left;
  width: 20%;
  padding: 10px;
  background: var(--primary-color);
  color: white;
  font-size: 18px;
  border: 3px solid var(--primary-color-dark);
  border-left: none; /* Prevent double borders */
  cursor: pointer;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}

.title-and-search-bar button,
.title-and-search-bar button:visited {
  display: inline-block;
  background: var(--primary-color);
  color: white;
  text-decoration: none;
  cursor: pointer;
}

.title-and-search-bar button:hover,
.title-and-search-bar button:active {
  background: var(--primary-color-dark);
  color: white;
}
@media (max-width: 600px) {
  header {
    flex-direction: column;
  }
}
</style>

<template>
  <header class="container">
    <section class="bookstore-logo">
      <div id="logo-image">
        <router-link to="/">
          <img
            src="@/assets/updateImage/site/headerLogo.jpg"
            alt=""
            width="174"
            height="auto"
          />
        </router-link>
      </div>
    </section>

    <section class="title-and-search-bar">
      <form action="category.html">
        <!--        <input type="text" class="search-bar" /><br />-->
        <!--        <input type="submit" class="button search-button" value="Search" />-->
        <form action="/" style="margin: auto; max-width: 300px">
          <input type="text" placeholder="search.." name="search" />
          <button type="submit" style="color: #111111">
            <font-awesome-icon icon="fa-magnifying-glass" />
          </button>
        </form>
      </form>
    </section>

    <section class="categories-cart-login">
      <button class="button">
        <header-dropdown></header-dropdown>
      </button>
      <button class="button">
        <font-awesome-icon icon="fa-cart-shopping" />
        cart
      </button>
      <button class="button">
        <font-awesome-icon icon="fa-user" />
        login
      </button>
    </section>
  </header>
</template>
