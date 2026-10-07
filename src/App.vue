<script setup>
import BlogPost from './BlogPost.vue';
import{ref} from 'vue';

const posts = ref([
  {title: 'Post 1', id: 1, body: 'descripcion 1'},
  {title: 'Post 2', id: 2, body: 'descripcion 2'},
  {title: 'Post 3', id: 3, body: 'descripcion 3'}
]);

const fav = ref('')

const cambiarFav = (post) => {
  fav.value = post
}

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


