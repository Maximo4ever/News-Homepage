<script setup>
import { ref } from "vue";

let navMenu = ref(null);
let iconMenu = ref(null);

const toggleMenu = () => {
  if (iconMenu.value.src.includes("close")) {
    iconMenu.value.setAttribute("src", "/icon-menu.svg");
    navMenu.value.classList.remove("active");
  } else {
    iconMenu.value.setAttribute("src", "/icon-menu-close.svg");
    navMenu.value.classList.add("active");
  }
};
</script>
<template>
  <nav class="nav">
    <img src="../assets/logo.svg" alt="Logo" />
    <div>
      <div class="nav__menu" ref="navMenu">
        <ul class="nav__menu__content">
          <li>Home</li>
          <li>New</li>
          <li>Popular</li>
          <li>Trending</li>
          <li>Categories</li>
        </ul>
      </div>
      <img
        class="nav__menu__icon"
        src="/icon-menu.svg"
        alt="Icon menu"
        ref="iconMenu"
        @click="toggleMenu"
      />
    </div>
  </nav>
</template>
<style>
.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 15px;
}
.nav__menu {
  display: flex;
  align-items: center;
  justify-content: center;
  list-style: none;
  gap: 30px;
}
.nav__menu.active {
  display: block;
  width: 100%;
  height: 100%;
  background: #0f1023ab;
  position: fixed;
  top: 0;
  left: 0;
}
.nav__menu.active + .nav__menu__icon {
  position: fixed;
  top: 22px;
  right: 15px;
}
.nav__menu__icon {
  display: none;
  width: 25px;
  height: 25px;
  position: relative;
  z-index: 22;
}
.nav__menu__content {
  list-style: none;
  font-size: 17px;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  column-gap: 30px;
}
.nav__menu.active .nav__menu__content {
  visibility: visible;
}
.nav__menu__content li {
  cursor: pointer;
  padding: 10px;
}
.nav__menu__content li:hover {
  color: var(--Soft-red);
}
@media (max-width: 1100px) {
  .nav__menu__icon {
    display: block;
  }
  .nav__menu__content {
    font-size: 18px;
    visibility: hidden;
    width: 65%;
    height: 100%;
    position: absolute;
    top: 0;
    right: 0;
    flex-direction: column;
    padding: 140px 30px 30px;
    row-gap: 20px;
    background: #ffffff;
    z-index: 11;
  }
}
</style>
