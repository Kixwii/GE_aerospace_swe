<template>
  <div>
    <h1>{{ title }}</h1>
    <img src="./assets/GE aerospace stock image.jpeg" alt="Image" width="200">
    <div>
      <label for="number1">Number 1:</label>
      <input type="number" id="number1" v-model="number1">
    </div>
    <div>
      <label for="number2">Number 2:</label>
      <input type="number" id="number2" v-model="number2">
    </div>
    <button v-if= "!showProduct" @click="computeProduct">Compute</button>
    <p v-if="showProduct">Product: {{ product }}</p>
  </div>
</template>

<script>
export default {
    data() {
    return {
      title: 'Compute Product',
      number1: 0,
      number2: 0,
      product: null,
      showProduct: false,
     };
    },
    methods:{
      computeProduct() {
          this.product = this.number1 * this.number2;
          this.showProduct = true;
      },
    },
  };
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
