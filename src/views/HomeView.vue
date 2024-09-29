<script setup>
import MonBouton from "../components/MonBouton.vue";
</script>

<template>
  <main>
    <div class="my-8">
      <MonBouton>Click</MonBouton>
      <MonBouton type="secondary">Click</MonBouton>
      <MonBouton type="danger">Click</MonBouton>
      <MonBouton type="danger" isDisabled>Click</MonBouton>
    </div>
  </main>
</template>
