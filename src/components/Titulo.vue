<template>
  <h1>Titulo dinamico: {{signoPeso}}</h1>
</template>

<script>
import { computed } from '@vue/reactivity';

export default {
    props: {
        contador: Number
    },
    setup(props){
        console.log(props.contador.contador);
        const signoPeso= computed(()=> {
            return '$' + props.contador;
        });


        return {
            signoPeso,
        }
    }
}
</script>

<style>

</style>