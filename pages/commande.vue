<template>
 <div>  
    <div class="card-deck">
     
    <h2 class= "display-4">Les produits disponibles</h2>
    <div v-for="produit in produits" class="card text-bg-dark mb-3" style="max-width: 18rem;">
      <div class="card-header">{{ produit.nom }}</div>
  <div class="card-body">
    <p class="card-text">Prix : {{ produit.prix }} </p>
  </div>
     </div>
  <nuxt />
  </div>
</div>
</template>

<script scoped>
export default{
    data(){
        return{
            produits:[
                {nom:"Pizza", prix:3.0},
                {nom:"Frites", prix:2.0},
                {nom:"Humburger", prix:2.5},
                {nom:"cheesburger", prix:3.0}
            ]
        }
    }
}
</script>

<style>

</style>