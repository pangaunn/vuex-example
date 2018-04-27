<template>
  <div id="app">
    <h1>Counter: {{ counter }}</h1>
    <h1>Counter + 8: {{ counterPlus8 }}</h1>
    <button @click="plus1Now">+1 Now</button>
    <button @click="plus1Later">+1 Later</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      counter: 1
    }
  },
  computed: {
    counterPlus8 () {
      return this.counter + 8
    }
  },
  methods: {
    plus1Now () {
      this.counter++
    },
    plus1Later () {
      setTimeout(() => {
        this.counter++
      }, 1000)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
