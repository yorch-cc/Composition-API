<script setup>
import ButtonCounter from './components/ButtonCounter.vue'
import BlogPost from './BlogPost.vue';
import{ref} from 'vue';

const posts = ref([
  {title: 'Post 1', id: 1, body: 'descripcion 1'},
  {title: 'Post 2', id: 2, body: 'descripcion 2'},
  {title: 'Post 3', id: 3, body: 'descripcion 3'}
]);

</script>

<template>
  <div class="container">
  <h1>Yorch</h1>
<ButtonCounter />
<button-counter />

<BlogPost 
v-for="post in posts"
:key="post.id"
    :title="post.title" 
    :id="post.id"
     :body="post.body" 
/>

</div>  
</template>

<style></style>


