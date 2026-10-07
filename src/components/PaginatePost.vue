<script setup>
    const emit = defineEmits(['next','prev'])
</script>

<template>  
 <div class="btn-group" role="group" aria-label="Basic example">
  <button @click="emit('prev')" type="button" class="btn btn-outline-primary">Previous</button>
  
  <button @click="emit('next')" type="button" class="btn btn-outline-primary">Next</button>


</div>
</template>