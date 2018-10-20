<template>
  <div id="app">

    {{ greeting }}
    <br/>
    <input v-model="message" placeholder="edit me">
    <p>Message is: {{ message }}</p>
    <br/>
    <button v-on:click="addToList()">Add item to List</button>
    <p>Show list: {{ list }}</p>

    <!--
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },

  data() {
    return {
    greeting: 'shakalaka',
    list: [],
    message: ''
    }
  },
  methods: {
    addToList() {
      this.list.push(this.message);
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
