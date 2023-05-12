

<script lang="ts">
import BaseCounter from "./components/BaseCounter.vue"
import UserCard from "./components/UserCard.vue"
  
  export default {
    components:{
      BaseCounter,
      UserCard
    },
    
    
        
  }
</script>

<template>
  <div>
    <a href="" @click.prevent="login" >login</a>
    <router-view />
   <!-- <BaseCounter  />
   <UserCard /> -->
   
  </div>
</template>
