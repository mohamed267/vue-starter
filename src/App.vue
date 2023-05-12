

<script lang="ts">
import UsersList from "./components/UsersList.vue"
  
  export default {
    components:{
      UsersList
    },
    
    
        
  }
</script>

<template>
  <div>
    <Suspense>
      <UsersList />

      
      <template #fallback>
        loding her
      </template>


    </Suspense>
   
   
  </div>
</template>
