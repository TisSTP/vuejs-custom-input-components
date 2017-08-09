<template>
  <input type="text"
      :value="value"
      @input="updateCode($event.target.value)" ref="inputRef">
</template>

<script>
export default {
  name: 'input3',
  props: ['value'],
  data() {
    return {
      invalids: ['test', 'tis', 'hello']
    }
  },
  methods: {
    updateCode(valInput) {
      // Validation
      if(this.invalids.includes(valInput)) {
        alert('Hello World.');

        // ทำให้ form input และ ตัวแปร valInput มีค่าเป็นค่าว่าง
        this.$refs.inputRef.value = valInput = '';

      }

      // ทำให้ค่าเปลี่ยนแปลง
      this.$emit('input', valInput);
    }
  }
}
</script>
