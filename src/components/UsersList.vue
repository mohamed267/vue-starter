<script lang="ts">
import { reactive, computed } from "vue"

export default {
  async setup() {

    const state =  reactive({
      usersList: []
    })

  
  
    
    async function fetchUsers(){
      const response = await  fetch("https://jsonplaceholder.typicode.com/users").then(res=>res.json())
      return response
    }
    state.usersList = await fetchUsers()
    return state


  },
  

  created() {
  }


}
</script>


<template>
    <ul>
          <li v-for="user in usersList" :key="user.id" >
            {{ user.name }}
    
          </li>
        </ul>


</template>
