<template>
  <div>
    <input v-model="message" placeholder="edit me">
    <p>Message is: {{ message }}</p>

    <button v-on:click="emitEvent()">Add item to List</button>
  </div>
</template>


<script>
export default {
  name: 'addProduct',

  data() {
    return {
      message: ''
      }
  },

  methods: {
    emitEvent() {
      this.$emit('add-product', this.message);
      console.log(this.message);
    }
  }
}
</script>
