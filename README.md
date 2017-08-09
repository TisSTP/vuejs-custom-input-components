# custom-input-components

> custom input component a Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

## example
> input example 1
``` html
<template>
  <input v-model="msg">
</template>

<script>
export default {
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
```

> input example 2
``` html
<template>
  <input :value="msg" @input="msg = $event.target.value">
</template>

<script>
export default {
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>
```

> input custom example
``` html
<template>
  <input type="text"
      :value="value"
      @input="updateCode($event.target.value)" ref="inputRef">
</template>

<script>
export default {
  name: 'input3',
  props: ['value'], // รับค่ามาจาก v-model
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
```
- `this.$refs.{refName}.value`
- `this.$emit('event', value)`


For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
