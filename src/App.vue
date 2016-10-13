<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1 v-on:click="click" v-if="seen">{{ msg }}</h1>
    <Hi v-bind:call="callBack" foo="foo222"></Hi>
  </div>
</template>

<script>
import Hi from './Hi.vue'

export default {
  data () {
    return {
      msg: 'Hello Vue!',
      seen: true
    }
  },
  methods: {
    click: function (e) {
      e.preventDefault();
      alert(this.msg)
    },
    callBack: function(data) {
      alert(`from sub data call foo ${data}`);
    }
  },
  components: {
    'Hi': Hi
  }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
</style>
