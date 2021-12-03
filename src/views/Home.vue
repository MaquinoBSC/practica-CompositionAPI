<template>
  <div class="home">
    <h1>Contador: {{ contador }}</h1>
    <button @click="disminuir()">Disminuir</button>
    <button @click="aumentar()">Aumentar</button>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  data(){
    return {
      contador: 0
    }
  },
  methods: {
    disminuir(){
      this.contador= this.contador - 1;
    },
    aumentar(){
      this.contador= this.contador + 1;
    }
  }
}
</script>
