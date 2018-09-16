<template>
  <div class="hero">
    <section v-on:click="_onClick($event)" class="hero-section">
      <h2 class="myH2">Tumble Roll</h2>
      <p>The hot new app for learning gymnastics</p>
      <button type="button">PUSH</button>
      <p>{{ inputText }}</p>
    </section>
  </div>
</template>

<script>
export default {
  name: 'TheHero',
  methods: {
    _onClick: ((event) => {
      event.preventDefault();
      if (event.target.tagName === 'BUTTON') {
        let myH2 = document.querySelector('.myH2');
        if (myH2.style.color === 'green') {
          myH2.style.color = 'white';
        } else {
          myH2.style.color = 'green';
        }
      }
    })
  },
  props: {
    inputText: String
  }
};
</script>

<style>
.hero-section {
  color: white;
  height: 90vh;
  background-image: url('../assets/mountains.jpg');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
