<template>
  <div class="about">
    <h1>Contador: {{ contador }} </h1>
    <button @click="disminuir()">Disminuir</button>
    <button @click="aumentar()">Aumentar</button>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity';

export default {
  setup(){
    const contador= ref(0);

    const aumentar= ()=> {
      contador.value++;
    }

    const disminuir= ()=> {
      contador.value--;
    }


    return {
      contador,
      disminuir,
      aumentar
    }
  }
}
</script>
