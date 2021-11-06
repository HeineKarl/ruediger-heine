<template>
  <router-link class="logo" to="/">
    <h1>Rüdiger Heine</h1>
  </router-link>
</template>

<script>
export default {
  name: "Logo",
};
</script>

<style lang="scss">
.logo {
  text-decoration: none;
  color: #2d2d2d;

  h1 {
    font-family: "Source Serif Pro", serif;
    font-weight: 900;
    font-size: 1em;
  }
}
</style>