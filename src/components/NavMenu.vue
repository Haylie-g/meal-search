<script setup lang="ts">
import HomePage from '@/views/HomePage.vue';
</script>

<template>
  <nav>
    <RouterLink :to="{ name: 'Home' }">Home</RouterLink>
    <RouterLink :to="{ name: 'MealsByName' }">Meals By Name</RouterLink>
    <RouterLink :to="{ name: 'MealsByLetter' }">Meals By Letter</RouterLink>
    <!-- Pass the required 'ingredient' parameter -->
    <RouterLink :to="{ name: 'MealsByIngredients', params: { ingredient: 'tomato' } }">
      Meals By Ingredients
    </RouterLink>
  </nav>
</template>


<style lang="postcss" scoped>
nav {
  @apply flex justify-center space-x-4;

  & .router-link-active {
    @apply underline underline-offset-4;
  }
}
</style>
