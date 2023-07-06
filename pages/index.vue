<template>
  <div class="home">
    <h1>
      Bem-Vindo(a) ao <span>{{ company }}</span>
    </h1>

    <NuxtLink to="/posts">Postagens</NuxtLink>
  </div>
</template>

<script>
import '/assets/main.css';
export default {
  data() {
    return {
      company: 'Blog'
    }
  }
}
</script>

<style>
  h1 {
    font-size: 2rem;
  }

  span {
    color: #2d6cea;
  }
</style>
