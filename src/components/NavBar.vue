<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";

const isOpen = ref(false);
const props = defineProps({
  links: {
    type: Array,
    default: () => [],
  },
});
</script>

<template>
  <nav>
    <button @click="isOpen = !isOpen">
      <i class="ri-menu-line"></i>
    </button>

    <ul v-show="isOpen" class="list-group mt-3">
      <li
        v-for="(link, index) in links"
        :key="`link-${index}`"
        class="list-group-item"
      >
        <RouterLink :to="link.lien">{{ link.titre }}</RouterLink>
      </li>
    </ul>
  </nav>
</template>
