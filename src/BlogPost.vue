<script setup>

 //defineProps(['title', 'id', 'body'])
 defineProps({
    title: String,
    id: Number,
    body: {
        type: String,
        default: "Sin descripcion",
    }
 })

 const emit = defineEmits(['cambiarFavNombre'])
 
 </script>



<template>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title"
            >{{id}}-{{ title }}</h5>
            <p>{{ body }}</p>
            <button @click="emit('cambiarFavNombre', title)" 
            class="btn btn-outline-primary ">
            Fav
         </button>
         </div>
    </div>
</template>