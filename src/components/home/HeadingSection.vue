<template>
  <div class="heading">
    <h1>Exponate der Fossiliensammlung</h1>
  </div>
</template>

<script>
export default {
  name: "HeadingSection",
};
</script>

<style lang="scss" scoped>
.heading {
  h1 {
    font-size: clamp(1.75rem, 1.4rem + 2vw, 2.25rem);
    font-family: "Source Serif Pro", serif;
    color: var(--heading-clr);
  }
}

@media screen and (min-width: 36em) {
  .heading {
    h1 {
      color: var(--heading-clr-darker);

      font-size: clamp(3rem, 2.25rem + 2vw, 4rem);
    }
  }
}

@media screen and (min-width: 49em) {
  .heading {
    h1 {
      text-align: center;
    }
  }
}
</style>