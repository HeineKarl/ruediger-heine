<template>
  <div class="header">
    <Logo />
    <IconBtn
      classBtn="burger-btn"
      classIcon="fas fa-bars"
      @click="handleSideBar"
    />
    <div class="nav" :class="sideBar ? 'open-nav' : null">
      <div class="nav-header">
        <IconBtn
          classBtn="close-btn"
          classIcon="fas fa-times"
          @click="handleSideBar"
        />
        <Logo @click="handleSideBar" />
      </div>
      <div class="nav-links">
        <NavLink @click="handleSideBar" txt="Home" link="/" />
        <NavLink @click="handleSideBar" txt="About" link="/about" />
        <NavLink @click="handleSideBar" txt="Blog" link="/blog" />
      </div>
    </div>
  </div>
  <router-view />
</template>


<script>
// Importing Hooks
import { ref } from "@vue/reactivity";

// Importing Components
import Logo from "./components/Logo.vue";
import IconBtn from "./components/IconBtn.vue";
import NavLink from "./components/NavLink.vue";

export default {
  name: "App",
  components: { Logo, IconBtn, NavLink },

  setup() {
    const sideBar = ref(false);

    function handleSideBar() {
      sideBar.value = !sideBar.value;
    }

    return { sideBar, handleSideBar };
  },
};
</script>

<style lang="scss">
:root {
  --txt-clr: #2d2d2d;
  --bg-clr: #eee;
  --font-pat: "Patua One", cursive;
  --font-src: "Source Serif Pro";
}
@mixin flex-center($justify: center, $dir: row) {
  display: flex;
  flex-direction: $dir;
  align-items: center;
  justify-content: $justify;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  height: 100vh;
  background: var(--bg-clr);
}

img {
  object-fit: cover;
  height: 100%;
  width: 100%;
}

// Header
.header {
  @include flex-center(space-between);
  height: 5em;
  padding: 1em 1.75em;
}

.nav {
  background: var(--bg-clr);
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  position: fixed;
  top: 0;
  right: 0;
  z-index: 1000;
  width: 16em;
  height: 100%;
}

.nav-header {
  @include flex-center();
  height: 5em;
  position: relative;
}

.close-btn {
  position: absolute;
  left: 10px;
}

.nav-links {
  @include flex-center(space-around, column);
  height: 18em;
}

//  Desktop
@media screen and (min-width: 49em) {
  .nav {
    @include flex-center();
    position: relative;
    box-shadow: none;
    width: 30em;
  }
  .burger-btn {
    display: none;
  }
  .nav-header {
    display: none;
  }

  .nav-links {
    @include flex-center(space-around, row);
    width: 100%;
    height: initial;

    a {
      padding: 1em;
    }
  }
}

// Animation and Transition
// Tablet and Phone View
@media screen and (max-width: 48em) {
  .nav {
    transform: translateX(17em);
    transition: transform 500ms ease;
  }

  .nav.open-nav {
    transform: translateX(0em);
  }
}
</style>
