<script lang="ts">
    export default {
        data() {
            return({
                count: 10
            })
        },
        methods: {
            increment() {
                this.count++;
            }
        }
    }
</script>


<template>
    {{count }}
    <button @click="increment" >icrement</button>

</template>