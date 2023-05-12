<script>
export default {
    props: {
        caracters:{
            type: Array,
            required: true,
        }
    },
    computed:{
        binderStatictics() {
            const elements =  [
            "Air",  
                "condition", 
                "signal" , 
                "apple"
            ]
            const stats = {
                Air:0 ,  
                condition:0, 
                signal: 0 , 
                apple: 0
            }

            this.caracters.forEach(caracter => {
                elements.forEach(element =>{
                    if(caracter.element.includes(element)){
                        stats[element] += 1;
                    }
                })
            });


            return stats;

        }
    }
}

</script>

<template>
<p>

    <ul>
        <li v-for="(stat, index ) in binderStatictics" :key="index" >
            {{ index}} -- {{stat}}

        </li>
    </ul>
</p>

</template>