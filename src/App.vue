<script setup>
import BlogPost from './BlogPost.vue';
import{ref} from 'vue';

const posts = ref([]);

const fav = ref('')

const cambiarFav = (post) => {
  fav.value = post
}

fetch('https://jsonplaceholder.typicode.com/posts')
.then((res) => res.json())
.then((data) => {
  posts.value = data})

</script>

<template>
  <div class="container">
  <h1>Yorch</h1>
  <h2>Mi Post Fav: {{ fav }}</h2>


<BlogPost 
v-for="post in posts"
:key="post.id"
    :title="post.title" 
    :id="post.id"
     :body="post.body" 
     @cambiarFavNombre ="cambiarFav"
/>

</div>  
</template>

<style></style>

