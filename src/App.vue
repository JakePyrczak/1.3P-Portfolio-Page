<script setup>
import { RouterLink, RouterView } from "vue-router";
import FooterComp from "./components/FooterComponent.vue";
import Dropdown from "./components/Dropdown.vue";
</script>

<template>
  <header class="h-wrapper">
    <div class="nav-style">
      <div class="main-nav">
        <RouterLink class="nav-link" to="/">Home</RouterLink> |
        <RouterLink class="nav-link" to="/about">About</RouterLink>
      </div>
      <div class="right-side">
        <RouterLink class="nav-link" to="/contact">Contact Me</RouterLink>
      </div>
    </div>

    <div class="mobile">
      <div class="nav-style-mod">
      <RouterLink class="nav-link" style="display: flex;" to="/">Jake's Portfolio</RouterLink>
    </div>
    <div class="mobile-button">
      <Dropdown  />
    </div>

  </div>
  </header>

  <div class="page-container">
    <div class="content-wrapper">
      <RouterView />
    </div>

    <footer>
      <FooterComp />
    </footer>
  </div>
</template>

<style scoped>
.h-wrapper {
  align-items: center;
  justify-content: space-between;
  width: 100%;
  max-width: 1100px;
  max-height: 100vh;
  border-bottom: 1px solid #acacac;
  background-color: rgb(238, 244, 255);
  position: fixed;
  z-index: 1;
}

.main-nav {
  display: flex;
  justify-content: center;
  padding: 10px 40px;
}

.nav-link {
  text-decoration: none;
  color: #3498db;
  transition: 0.4s;
  padding: 0 20px;
  margin: 0 10px;
}

.nav-link:hover {
  color: #db2929;
}

.nav-link.router-link-active {
  color: #202f83;
  position: relative;
}

.nav-link.router-link-active::before {
  content: "";
  /*Create an empty pseudo-element */
  position: absolute;
  /* Set absolute positioning */
  bottom: -25px;
  /* Adjust this value to align with the header line */
  left: 0;
  /* Align the pseudo-element with the link text */
  width: 100%;
  /* Make the pseudo-element span the full width */
  border-bottom: 2px solid #202f83;
  /* Add the underline styling */
}

.nav-style {
  font-size: 1.05rem;
  padding: 13px 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-style-mod {
  font-size: 1.05rem;
  padding: 13px 20px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.right-side {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  margin: 0 2rem;
  padding: 10px 20px;
}

.page-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  /* This ensures the container takes at least most of the viewport */
}

.content-wrapper {
  flex: 1;
  /* This makes the content take up all available space, pushing the footer to the bottom */
  margin: 70px 7%;
}

footer {
  margin-top: 30px;
}

.mobile {
  display: none;
}

/* Media query for small screens */
@media (max-width: 882px) {
  .mobile-button {
    display: flex;
    padding: 0 25px;
    justify-content: flex-end;
    text-align: center;
    margin-top: 11px;
    margin-bottom: 14px;
    margin-right: 30px;
  }

  .mobile {
    display: flex;
  }

  .nav-style {
    display: none;
  }

  .content-wrapper {
    margin: 70px 5%;
  }

  footer {
    margin-top: 20px;
  }
}
</style>
