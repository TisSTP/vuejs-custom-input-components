<template>
  <div>
     <input v-model="msg">
    <!-- <input :value="msg" @input="msg = $event.target.value"> -->
  </div>
</template>

<script>
export default {
  name: 'input1',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
