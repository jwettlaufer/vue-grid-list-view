<template>
  <div id="app">
   <h1>Grid / List View</h1>
   <Fruits :fruits={fruits} />
  </div>
</template>

<script>
import Fruits from './components/Fruits.vue';

export default {
  name: 'App',
  components: {
    Fruits
  },
  data(){
    return {
    fruits: [
      'Apple',
      'Banana',
      'Orange',
      'Pear',
      'Cherry',
      'Peach',
      'Mango',
      'Lemon',
      'Lime'
    ]
    }
  }
}
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
