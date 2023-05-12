<script lang="ts">
    import { count } from "../composables/counterStore"
    export default {
        setup() {
            return{
                count
            }

        },
        methods: {
            increment() {
                this.count++;
            }
        }
    }
</script>


<template>
    <p>
        {{count }}

    </p>
    <p>
        <button :class="$style.button" @click="increment" >icrement</button>

    </p>
   

</template>

<style module >
.button {
    background-color: aqua;
}

</style>