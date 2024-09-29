<script setup>
import { RouterView } from "vue-router";
import NavBar from "./components/NavBar.vue";

const navLinks = [
  { titre: "Home", lien: "/" },
  { titre: "About", lien: "/about" },
  { titre: "Contact", lien: "/contact" },
];
</script>

<template>
  <header>
    <div class="wrapper">
      <NavBar :links="navLinks" />
    </div>
  </header>

  <RouterView />
</template>
