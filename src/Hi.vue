<template>
  <div id="hi">
    <h1 v-on:click="click">{{ msg }}{{ foo }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    foo: {
      type: String
    },
    call: Function
  },
  data () {
    return {
      msg: 'i am hi component'
    }
  },
  methods: {
    click: function(e) {
      e.preventDefault();
      this.call('hihihi')
    }
  }
}
</script>

<style>
#hi {
  background-color: red
}
</style>
