<template>
  <div id="app">
    <img src="./assets/logo.png">
    {{$store.state.count}}
    <br>
    {{addCount()}}
    <!-- {{$store.actions.addCount}} -->
  </div>
</template>

<script>
export default {
  name: 'App',
  mounted(){
    console.log(this.$store.state)
  },
  methods:{
    addCount(){
      this.$store.dispatch('addCount',1000)
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
