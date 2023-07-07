<template>
    <div>
        <h1 v-if="post">{{ post.title }}</h1>
        <p v-if="post">{{ post.description }}</p>
        <h3 v-else>Post não existe.</h3>
    </div>
</template>
  
<script>
import '/assets/main.css';

export default {
    head() {
        return {
      title: this.post ? this.post.title : 'Postagem não existe...'
    };
  },
  
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
  
<style scoped>
h1, p{
    cursor: default;
}
    h3 {
        color: #000;
        width: max-content;
        position: relative;
        margin: 1rem 0;
        cursor: default;
        font-size: 2rem;
    }

    h3:before {
        content: '';
        background-color: #ea2d2d;
        width: 105%;
        height: 30%;
        position: absolute;
        bottom: 1px;
        left: 50%;
        transform: translatex(-50%);
        z-index: -1;
        transition: height 0.1s linear;
        opacity: 0.4;
        cursor: default;
    }

    h3:hover:before {
        height: 100%;
        cursor: default;
    }
</style>
  