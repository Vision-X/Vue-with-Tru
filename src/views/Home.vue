<template>
  <div class="home">
    <TheHeader />
    <TheHero v-bind:inputText="inputData"/>
    <input v-on:keyup="_onChange" class="text-input"></input>
  </div>
</template>

<script>
// @ is an alias to /src

import TheHeader from '@/components/TheHeader.vue'
import TheHero from '@/components/TheHero.vue';
export default {
  name: 'home',
  components: {
    TheHeader,
    TheHero
  },
  data() {
    return {
      inputData: ''
    }
  },
  methods: {
    _onChange: function() {
      let typedText = document.querySelector('.text-input').value;
      this.inputData = typedText;
    },
    _fetchShoes: function() {
      console.log("hi, this is the fetch method");
    }
  }
};
</script>
