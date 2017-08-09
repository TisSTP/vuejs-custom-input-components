<template>
  <div>
     <input :value="msg" @input="msg = $event.target.value">
  </div>
</template>

<script>
export default {
  name: 'input2',
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
