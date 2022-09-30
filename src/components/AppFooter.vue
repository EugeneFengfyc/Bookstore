<script setup lang="ts"></script>

<style scoped>
footer {
  background: #ffffff;
  display: flex;
  gap: 1em;
  width: 1200px;
  height: 100px;
  margin-top: 5px;
  justify-content: space-between;
}

.copy-right {
  background-color: #ffffff;
  text-align: left;
  float: left;
  font-size: 15px;
  color: #000000;
  padding: 5px;
  margin-top: 16px;
}

.links {
  text-align: center;
}

.media {
  text-align: right;
}

.but {
  display: inline-block;
  background: var(--primary-color);
  color: white;
  padding: 0.5em 0.5em;
  cursor: pointer;
  border: 2px none;
  border-radius: 50px;
  width: 50px;
  height: 50px;
  font-size: 25px;
  margin-top: 5px;
}
.link-text {
  font-size: 20px;
  color: #000000;
  text-decoration: none;
  margin-top: 20px;
}
.social-media-icons {
  flex-direction: row;
  text-align: center;
}
</style>

<template>
  <footer class="container">
    <section class="copy-right">
      <font-awesome-icon icon="fa-regular fa-copyright" /> HIKARI All Rights
      Reserved
    </section>
    <section class="links">
      <div class="link-text">
        <router-lin to="/" style="position: relative; margin-right: 20px">
          About
        </router-lin>
        <h8>|</h8>
        <router-link to="/" style="margin-left: 20px; margin-right: 20px"
          >Contact</router-link
        >
        <h8>|</h8>
        <router-link to="/" style="position: relative; margin-left: 20px">
          Direction
        </router-link>
      </div>
    </section>
    <section class="media">
      <div class="social-media-icons" style="position: relative; right: 25px">
        <router-link to="/" class="but" style="color: #111111">
          <font-awesome-icon icon="fa-brands fa-facebook" />
        </router-link>
        <router-link to="/" class="but" style="color: #111111">
          <font-awesome-icon icon="fa-brands fa-instagram" />
        </router-link>
        <router-link to="/" class="but" style="color: #111111">
          <font-awesome-icon icon="fa-brands fa-twitter" />
        </router-link>
      </div>
    </section>
  </footer>
</template>
