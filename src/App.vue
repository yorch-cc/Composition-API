<script setup>
import{ref} from 'vue';
import BlogPost from './BlogPost.vue';
import PaginatePost from './components/PaginatePost.vue';

const posts = ref([]);

const fav = ref('')

const postXPage = 10

const inicio = ref(0)

const fin = ref(postXPage)

const cambiarFav = (post) => {
  fav.value = post
}

const next = () => {
  inicio.value = inicio.value + postXPage
  fin.value = fin.value + postXPage
}

const prev = () =>{
  inicio.value = inicio.value - postXPage
  fin.value = fin.value - postXPage
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

  

  <PaginatePost @next="next" @prev="prev" class="mb-2"/>



<BlogPost 
v-for="post in posts.slice(inicio, fin)"
:key="post.id"
    :title="post.title" 
    :id="post.id"
     :body="post.body" 
     @cambiarFavNombre ="cambiarFav"
     class="mb-2"
/>

</div>  
</template>

<style></style>

