<template>
    <div class="posts">
      <ul>
        <li v-for="post in posts" :key="post.id">
          <NuxtLink :to="`/post/${post.id}`">
            <h2>{{ post.title }}</h2>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  import '/assets/main.css';
  export default {
    data() {
      return {
        posts: [
          {
            id: 1,
            title: 'Construindo Front-End',
            description: 'Descrição da Postagem 1'
          },
          {
            id: 2,
            title: 'SSR com Nuxt.js',
            description: 'Descrição da Postagem 2'
          },
          {
            id: 3,
            title: 'API com Adonis.js',
            description: 'Descrição da Postagem 3'
          },
          {
            id: 4,
            title: 'Deploy de aplicações',
            description: 'Descrição da Postagem 4'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  li{
    list-style: none;
  }
  </style>
  