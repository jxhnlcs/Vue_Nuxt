<template>
    <div>
        <h1 v-if="post">{{ post.title }}</h1>
        <p v-if="post">{{ post.description }}</p>
        <h1 v-else>Post não existe.</h1>
    </div>
</template>
  
<script>
import '/assets/main.css';

export default {
    data() {
        return {
            post: null,
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
        };
    },


    async fetch() {
        const postId = this.$route.params.id;
        const foundPost = this.posts.find((post) => post.id === parseInt(postId));
        this.post = foundPost ? foundPost : null;
    }
};

</script>
  
<style scoped></style>
  