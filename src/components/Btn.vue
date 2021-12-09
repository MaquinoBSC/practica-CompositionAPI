<template>
  <button @click="accionHijo">{{ textoBoton }}</button>
</template>

<script>
export default {
    props: {
        textoBoton: { type: String },
    },
    setup(props, context){
        const accionHijo= ()=> {
            context.emit('accion');
        }

        return {
            accionHijo
        }
    }
}
</script>

<style>

</style>