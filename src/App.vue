<template>
  <div id="app">
    <adding-field></adding-field>
  </div>
</template>

<script>
import addingField from './components/adding-field'

export default {
  name: 'app',
  components: {
    addingField,
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  outline: none;
}

body {
  margin: 0;
}

</style>
