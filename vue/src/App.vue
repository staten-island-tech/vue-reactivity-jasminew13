<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>

  <RouterView />  
</template>

<style scoped>

header {
  line-height: 1.5;

}


@media (min-width: 1024px) {
  header {
    display: flex;
    padding-right: calc(var(--section-gap) / 2);
  }

/*  .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  } */

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
