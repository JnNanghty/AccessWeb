<template>
  <div id="app">
    <input type="text" v-model="url">
    <button @click="go">GO</button>
    <iframe class="frame" ref="frame"></iframe>
  </div>
</template>

<script>


export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      url: ''
    }
  },
  methods: {
    go() {
      this.$refs.frame.src = this.url;
    }
  }
}
</script>

<style>
.frame{
  width: 100%;
  height: 100vh;
}
</style>
