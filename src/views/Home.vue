<style>
.frame{
  width: 100%;
  height: 100vh;
}
</style>
<template>
  <div class="home">
    <input type="text" v-model="url">
    <button @click="go">go</button>
    <iframe class="frame" ref="frame"></iframe>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data() {
    return {
      url: ''
    }
  },
  components: {},
  mounted() {
    this.$refs.frame.src = this.url
  },
  methods: {
    go() {
      this.$refs.frame.src = this.url
    }
  }
}
</script>
