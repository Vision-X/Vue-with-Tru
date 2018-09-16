<template>
  <div class="home">
    <TheHeader />
    <TheHero v-bind:inputText="inputData" />
    <input v-on:keyup="_onChange" class="text-input"></input>
    <div v-if="loaded">
      <TheShoes v-bind:shoes="shoeData" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import TheHeader from '@/components/TheHeader.vue'
import TheHero from '@/components/TheHero.vue';
import TheShoes from '@/components/TheShoes.vue';
export default {
  name: 'home',
  components: {
    TheHeader,
    TheHero,
    TheShoes,
  },
  data() {
    return {
      inputData: '',
      shoeData: [],
      loaded: false
    }
  },
  methods: {
    _onChange() {
      let typedText = document.querySelector('.text-input').value;
      this.inputData = typedText;
    },
    _fetchShoes() {
      console.log("hi, this is the fetch method");
      let url = "https://webscraper-to-api.firebaseapp.com/output.json"
      let dataGetter = response => {
        let arr = [];
        for (let key in response) {
          arr.push(response[key])
        }
        this.shoeData = arr;
        this.loaded = true;
        this._logState();
      }
      return fetch(url)
             .then(response => response.json())
             .then(dataGetter)
             .catch(console.error);
    },
    _logState() {
      console.log("hmmm", this.shoeData);
    }
  },
  mounted() {
    this._fetchShoes();
  }
};
</script>
