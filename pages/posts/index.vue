<template>
    <div class="posts">
        <ul>
            <li v-for="post in posts" :key="post.id">
                <PostPreview :id="post.id" :title="post.title" />
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
    },
    head(){
        return {
            title: 'Posts do Blog',
            meta: [
                {
                    hid: 'description',
                    name: 'descripton',
                    content: 'Descrição do meu Blog legal'
                }
            ]
        }
    }
}
</script>
  
<style scoped>
li {
    list-style: none;
}
</style>
  