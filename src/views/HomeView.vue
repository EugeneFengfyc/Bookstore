<script setup lang="ts">
import HomeCategoryList from "@/components/HomeCategoryList.vue";
</script>

<style scoped>
.home-page {
  display: flex;
  width: 1200px;
  height: 500px;
  justify-content: space-between;
}

.welcome-text {
  width: 15em;
  margin-top: 10px;
  font-size: 30px;
  color: #807974;
  text-align: left;
}

.category-image {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 1em;
  float: right;
  text-align: right;
}

.home-button,
.home-button:visited {
  display: inline-block;
  background: var(--primary-color-dark);
  color: #000000;
  text-decoration: none;
  padding: 0.5em 0.5em;
  cursor: pointer;
  border: 2px none;
  font-size: 2rem;
}

.home-button:hover,
.home-button:active {
  background: var(--primary-color-dark);
  color: #000000;
}
</style>
<template>
  <div class="home-page">
    <section class="welcome-text container">
      <div style="position: relative; width: 590px; height: 500px">
        <img
          src="@/assets/updateImage/site/welcomeManImage.png"
          width="800px"
          height="auto"
          alt=""
        />
      </div>
    </section>
    <section class="flow-content container">
      <div style="position: relative; margin-top: 40px; margin-right: 100px">
        <img src="@/assets/updateImage/site/welcomeRight.png" alt="" />
        <div style="position: absolute; margin-top: 120px; margin-left: 100px">
          <button class="home-button">SHOP NOW</button>
        </div>
      </div>
    </section>
  </div>
</template>
