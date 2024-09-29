<script setup>
import { ref } from "vue";
const nom = ref("");
const email = ref("");
const sujet = ref("");
const message = ref("");
const show = ref(false);
</script>

<template>
  <h2 class="mt-3">Nom :</h2>
  <input v-model="nom" class="border-solid border-2 border-black" />
  <h2 class="mt-3">Email :</h2>
  <input v-model="email" class="border-solid border-2 border-black" />
  <h2 class="mt-3">Sujet :</h2>
  <input v-model="sujet" class="border-solid border-2 border-black" />
  <h2 class="mt-3">Message :</h2>
  <input v-model="message" class="border-solid border-2 border-black" />

  <button
    class="border-solid border-2 border-black ml-10"
    @click="show = !show"
  >
    Envoyer
  </button>
  <div v-show="show">
    <div>Nom : {{ nom.length > 0 ? nom : "null" }}</div>
    <div>Email : {{ email.length > 0 ? email : "null" }}</div>
    <div>Sujet : {{ sujet.length > 0 ? sujet : "null" }}</div>
    <div>Message : {{ message.length > 0 ? message : "null" }}</div>
  </div>
</template>
