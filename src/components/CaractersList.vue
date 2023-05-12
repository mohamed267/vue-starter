<script>
    export default {
        props:['caracters', 'favourites'],
        emits:["addFavouriteCaracters"]
    }

</script>

<template>
    <ul>
      <li  v-for="(caracter , index) in caracters" :key="index" @click="$emit('addFavouriteCaracters', caracter)"  >
        {{ caracter.name }}
      </li>

      <p> favourite caracters </p>

      <li  v-for="(caracter , index) in favourites" :key="index" >
        {{ caracter.name }}
      </li>
    </ul>

</template>