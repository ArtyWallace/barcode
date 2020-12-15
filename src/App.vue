<template>
  <div id="app">
    <qrcode-stream @decode="onDecode"></qrcode-stream>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    result: null
  }),
  methods: {
    onDecode (val) {
      this.result = val
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
  margin: 60px auto 0;
}
</style>
