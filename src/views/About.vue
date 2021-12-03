<template>
  <div class="about">
    <h1 :style="{'color': setColor}">Contador: {{ contador }} </h1>
    <button @click="disminuir()">Disminuir</button>
    <button @click="aumentar()">Aumentar</button>
  </div>
</template>

<script>
import { computed, ref } from '@vue/reactivity';

export default {
  setup(){
    const contador= ref(0);

    const aumentar= ()=> {
      contador.value++;
    }

    const disminuir= ()=> {
      contador.value--;
    }

    const setColor= computed(()=> {
       return contador.value > 0 ? 'blue' : 'red'
    });


    return {
      contador,
      disminuir,
      aumentar,
      setColor,
    }
  }
}
</script>
