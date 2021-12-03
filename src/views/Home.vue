<template>
  <div class="home">
    <h1 :style="{'color': setColor}">Contador: {{ contador }}</h1>
    <button @click="disminuir()">Disminuir</button>
    <button @click="aumentar()">Aumentar</button>
  </div>
</template>

<script>

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
  },
  computed: {
    setColor(){
      return this.contador > 0 ? 'blue' : 'red';
    }
  }
}
</script>
