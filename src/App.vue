

<script lang="ts">
  export default {
    components:{
    },
    data(){
      return(
        {
          pokedex: [ 1, 2,3 ]
        }
      )
    },
    methods: {
      async fetchPok(){

        this.pokedex =await fetch("https://pokeapi.co/api/v2/pokemon/ditto").then(res=>res.json())
      
      }
    }, 
    created(){
      this.fetchPok()
    }
    
        
  }
</script>

<template>
  <div>
    {{  pokedex }}

    <button  @click="fetchPok">
      submit
    </button>
   
  </div>
</template>


<docs>
  
</docs>