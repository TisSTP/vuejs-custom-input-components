<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <input1></input1>
    <input2></input2>
    <input3 v-model="coupon"></input3>
  </div>
</template>

<script>
import Input1 from './components/Input1'
import Input2 from './components/Input2'
import Input3 from './components/Input3'

export default {
  name: 'app',
  components: {
    Input1, Input2, Input3
  },
  data() {
    return {
      coupon: 'FREE'
    }
  }
}
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
