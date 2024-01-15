<template>
         
       <div class="card text-white bg-dark mb-3" style="max-width: 18rem;">
         <div class="card-header">{{ nom }}</div>
     <div class="card-body">
       <p class="card-text">Prix : {{ prix }} </p>
       <hr>
       <button v-if="role== 'Commander'"  @click="$emit('commande', nom, prix)" class="btn btn-success">Commander!</button>
     </div>
     <nuxt />
        </div>
    
   </template>

   <script setup >
     const props = defineProps(["nom","prix","role"]);
          
  </script>