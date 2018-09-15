<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from './views/Home.vue';
export default {
  name: 'App',
  components: {
    Home
  },
  // data() {
  //   return (
  //     this.state.inputTitle
  //   )
  // },
  // created: (() => {
  //   this._fetchShoes();
  // }),
  // methods: {
  //   _fetchShoes: (() => {
  //
  //   }),
  //   _onChange: (() => {
  //
  //   })
  // },
};
</script>

<style>
* {
  margin: 0;
}
</style>
