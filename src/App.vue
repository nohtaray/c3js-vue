<template>
  <div id="app">
    <img src="./assets/logo.png">
    <stackbar />
    <donut />
  </div>
</template>

<script>
  import stackbar from './components/Stackbar';
  import donut from './components/Donut';

  export default {
    name: 'App',
    components: {
      donut,
      stackbar,
    },
  };
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
