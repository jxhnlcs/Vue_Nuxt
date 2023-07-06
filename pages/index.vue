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

<style scoped>
h1 {
  font-size: 2rem;
}

span {
  color: #2d6cea;
}

a {
  color:
    #000;
  width: max-content;
  position: relative;
  margin: 1rem 0;
  font-size: 1.5rem;
  font-weight: bold;
}

a:before {
  content: '';
  background-color: #2d6cea;
  width: 105%;
  height: 30%;
  position: absolute;
  bottom: 1px;
  left: 50%;
  transform: translatex(-50%);
  z-index: -1;
  transition: height 0.1s linear;
  opacity: 0.4;
}

a:hover:before {
  height: 100%;
}
</style>
