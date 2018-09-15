<template>
  <div class="header">
    <header>
      <h1>TumbleRoll.com</h1>
      <nav>
        <ul>
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/contact">Contact</router-link></li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  name: 'TheHeader',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  background-color: blue;
  color: white;
  height: 10vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

ul {
  display: flex;
  justify-content: space-between;
  width: 50%;
}

li {
  list-style-type: none;
  padding: 1rem;
}

a {
  color: white;
  text-decoration: none;
}
</style>
