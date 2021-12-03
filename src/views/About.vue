<template>
  <div class="about">
    <Titulo :contador="contador" />
    <h1 :style="{'color': setColor}">Contador: {{ contador }} </h1>
    <button @click="disminuir()">Disminuir</button>
    <button @click="aumentar()">Aumentar</button>
    <hr>

    <input type="text" v-model="texto">
    <p>{{ texto }}</p>
  </div>
</template>

<script>
import { computed, ref } from '@vue/reactivity';
import Titulo from '../components/Titulo.vue';

export default {
  components: {
    Titulo
  },
  setup(){
    const contador= ref(0);
    const texto= ref('');

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
      texto,
    }
  }
}
</script>
