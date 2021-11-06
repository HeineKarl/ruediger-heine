<template>
  <div class="home-about">
    <div class="about-image">
      <img src="../../assets/image1.png" alt="Purple Fossil" />
    </div>
    <div class="about-content">
      <p>
        Welcome to the life blog of Rudiger Heine that exhibits his Fossils
        collections from the start up to today. He seize the day with more
        informational blogs regarding to species and categories of the life
        before us.
      </p>
      <router-link to="/about">
        Learn More
        <i class="fas fa-long-arrow-alt-right"></i>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutSection",
  props: {},
  setup() {},
};
</script>

<style lang="scss">
.home-about {
  display: grid;
  grid-template-columns: 2fr 1fr 4em;
  grid-template-rows: 10em 14em 8em;
}

.about-content {
  background-color: #462a4c;
  border-radius: 0.5rem;

  padding: 9em 1em 5em 1em;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  grid-row: 1 / 3;
  grid-column: 1 / 3;

  p,
  a {
    font-family: "Source Serif Pro", serif;
    font-size: clamp(0.8rem, 0.35rem + 2vw, 0.85rem);
    color: white;
  }
}

.about-image {
  align-self: center;
  max-width: 12em;

  grid-row: 2 / 4;
  grid-column: 2 / 4;
  z-index: 2;
}

.fa-long-arrow-alt-right {
  font-weight: 600;
  padding-left: 0.5em;
}

@media screen and (min-width: 26.5em) {
  .home-about {
    grid-template-rows: 10em 12em 8em;
  }
}
@media screen and (min-width: 36em) {
  .home-about {
    grid-template-rows: 12em 2em;
    grid-template-columns: 2fr 1fr 4em;
  }
  .about-content {
    padding: 3em 10em 3em 1em;

    p,
    a {
      font-size: clamp(0.85rem, 0.15rem + 2vw, 0.95rem);
    }
  }

  .about-image {
    justify-self: end;
    max-width: 14em;
    grid-row: 1 / 3;
    grid-column: 2 / 4;
  }
}

@media screen and (min-width: 49em) {
  .about-content {
    max-width: 40em;
  }
}
</style>