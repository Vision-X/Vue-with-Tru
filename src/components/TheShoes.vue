<template>
  <section>
    <ul>
      <li v-for="shoe in shoes">
        <p>{{ shoe.name }}</p>
        <p>{{ shoe.relDate }}</p>
      </li>
    </ul>
  </section>
</template>


<script>
export default {
  name: 'TheShoes',
  props: {
    shoes: {
      type: Array,
      required: true
    },
  }
};
</script>


<style>
li {
  list-style-type: none;
  padding: 1rem;
}
</style>
