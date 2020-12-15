<template>
  <div>
    <qrcode-qrcode-stream @decode="onDecode"></qrcode-qrcode-stream>
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
  margin-top: 60px;
}
</style>
