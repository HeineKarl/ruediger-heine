<template>
  <div class="home">
    <HeadingSection class="home__heading" />
    <AboutSection class="home__about" />
    <ShopSection />
    <div class="spass"><h1>Nothing to See here yet</h1></div>
  </div>
</template>

<script>
import HeadingSection from "../components/home/HeadingSection.vue";
import AboutSection from "../components/home/AboutSection.vue";
import ShopSection from "../components/home/ShopSection.vue";
import IconBtn from "../components/IconBtn.vue";

export default {
  name: "Home",
  components: { HeadingSection, AboutSection, ShopSection, IconBtn },
};
</script>

<style lang="scss"  >
:root {
  --heading-clr: #edae75;
  --heading-clr-darker: #a0622c;
  --about-clr: #462a4c;
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
.spass {
  @include flex-center();
  height: 30rem;
}

.home {
  padding: 0 1.75em;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 10em 20em;

  &__heading {
    @include flex-center(null, column);
    padding-left: 1em;
    align-self: center;

    grid-column: 1 / -1;
    grid-row: 1 / 2;
    z-index: 2;
  }

  &__about {
    grid-column: 1 / -1;
    grid-row: 1 / 3;
    max-width: 24em;
  }
}

@media screen and (min-width: 26.5em) {
  .home {
    justify-items: center;

    &__heading {
      justify-self: start;
    }

    &__about {
      max-width: initial;
    }
  }
}

@media screen and (min-width: 36em) {
  .home {
    &__heading {
      padding-left: 0;
    }

    &__about {
      grid-row: 2 / 3;
      align-self: center;
    }
  }
}
// Tablet to Desktop
@media screen and (min-width: 49em) {
  .home {
    grid-template-rows: 15em 20em;
    &__heading {
      justify-self: center;
      max-width: 40em;
    }
  }
}
</style>
