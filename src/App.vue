<script setup>
import ButtonCounter from './components/ButtonCounter.vue'
import BlogPost from './BlogPost.vue';

</script>

<template>
  <div class="container">
  <h1>Yorch</h1>
<ButtonCounter />
<button-counter />

<BlogPost 
    title="Post 1" id="1" body="descripcion 1" colorText="primary"
/>
<BlogPost 
    title="Post 2" id="2"  body="descripcion 2" colorText="secondary"
/>

<BlogPost 
  title="Post 3" id="3"  body="descripcion 3" colorText="success"
/>
</div>  
</template>

<style></style>


