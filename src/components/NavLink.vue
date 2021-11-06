<template>
  <router-link class="nav-link" :to="link">{{ txt }}</router-link>
</template>

<script>
export default {
  name: "NavLink",
  props: {
    txt: String,
    link: String,
  },
};
</script>

<style lang="scss">
.nav-link {
  text-decoration: none;
  color: #2d2d2d;
}
</style>