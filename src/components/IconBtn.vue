<template>
  <button :class="classBtn" class="icon-btn">
    <router-link v-if="showTxt" :to="to"
      ><span>{{ txt }}</span></router-link
    >
    <i v-else :class="classIcon"></i>
  </button>
</template>

<script>
export default {
  name: "IconBtn",
  props: {
    classIcon: {
      type: String,
      default: "fas fa-times",
    },
    classBtn: {
      type: String,
      default: "icon-btn",
    },
    showTxt: {
      type: Boolean,
      default: false,
    },
    txt: {
      type: String,
      default: "Explore",
    },
    to: {
      type: String,
      default: "/",
    },
  },
};
</script>

<style lang="scss">
.icon-btn {
  --area: 2.5em;
  width: var(--area);
  height: var(--area);
  color: #2d2d2d;
  outline: 0;
  border: 0;
  border-radius: 50%;
  cursor: pointer;

  transition: background 200ms ease;

  &:active {
    background: #d3d3d3;
  }

  i {
    font-size: 1.25em;
    border-radius: 1em;
  }

  a {
    text-decoration: none;

    &:active {
      background: #d3d3d3;
    }
  }
}
</style>