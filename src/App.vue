<template>
  <div id="app">
    <qrcode-stream class="qr" @decode="onDecode"></qrcode-stream>
    <div>{{ result }}</div>
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

.qr {
  width: 200px;
  height: 200px;
  margin-bottom: 20px;
}
</style>
