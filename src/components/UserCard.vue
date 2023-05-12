<script lang="ts">
    import { count } from "../composables/counterStore"
    export default {
        setup() {
            return{
                count
            }

        },
    }
</script>


<template>
    {{count }}
    <button>scoep</button>

</template>