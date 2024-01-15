<template>
 <div>  
  
    <h1 class="display-1"></h1>
    <h2>Produits disponible</h2>
    <div class="card-deck">
   <Produit v-for="produit in produits" v-bind:nom="produit.nom"  v-bind:prix="produit.prix"  role="Commander" v-on:commande="ajouterProduit"/>
  </div>

    <h2>Produits commandés</h2>
    <div class="card-deck">
     <Produit v-for="produit in commandes" v-bind:nom="produit.nom" v-bind:prix="produit.prix" role="Affichage" />
    </div>
    <nuxt />
</div>
</template>

<script scoped>
import Produit from '@/components/Produit.vue'
export default{
   components:{
    Produit
   },
    data(){
        return{
            produits:[
                {nom:"Pizza", prix:3.0},
                {nom:"Frites", prix:2.0},
                {nom:"Humburger", prix:2.5},
                {nom:"cheesburger", prix:3.0}
            ],
            commandes:[
                {nom:"Pizza", prix:3.0}
            ]
        }
    },
    methods:{
        ajouterProduit(nom,prix){
            this.commandes.push({nom:nom, prix:prix})
        }
    }

}
</script>

<style>

</style>