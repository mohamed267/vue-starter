

<script lang="ts">
  import BaseCounter from "./components/BaseCounter.vue"
  import  BidStats  from "./components/BindStaticstics.vue";
  import CaractersList from "./components/CaractersList.vue";
  import BaseTemplate from "./components/templates/BaseTemplate.vue"
  export default {
    components:{
      BaseCounter,
      BidStats,
      CaractersList,
      BaseTemplate
    },
    data(){
      return(
        {
          message: "here is going our message",
          caractersList: [
            { name: "john", element: ["Air", "condition"] },
            { name: "dib" , element: ["signal", "apple"] }
          ],
          favouriteCaracters: [],
        }
      )
    },
    
        
    methods:{
            addFavouriteCaracters(caracter){
                this.favouriteCaracters.push( caracter);
            }
      },
  }
</script>

<template>
  <div>
    <BaseTemplate>
    fofo
      <template v-slot:header >
        temp o
      </template>
  </BaseTemplate>
    <BaseCounter />
    <p>
      {{ message }}
    </p>

    <BidStats  :caracters="caractersList" />

    <CaractersList :caracters="caractersList"
    
      :favourites="favouriteCaracters"
      @addFavouriteCaracters="addFavouriteCaracters"
    />
    
   
  </div>
</template>


<docs>
  
</docs>