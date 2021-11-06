<template>
  <div class="grid">
    <h1>Settlement</h1>
    <div class="content">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Purus viverra
        aliquet habitant dui diam, lacus a proin. Risus, pellentesque urna
        elementum non orci interdum sed pellentesque proin. Consequat, turpis
        lacus, ut pulvinar. Lobortis nulla urna augue elit.
      </p>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Purus viverra
        aliquet habitant dui diam, lacus a proin. Risus, pellentesque urna
        elementum non orci interdum sed pellentesque proin. Consequat, turpis
        lacus, ut pulvinar. Lobortis nulla urna augue elit.
      </p>
    </div>
    <div class="img-container">
      <img src="../../assets/image2.png" alt="Teeth" />
    </div>
  </div>
</template>

<script>
export default {
  name: "ShopSection",
};
</script>

<style lang="scss" scoped>
@mixin flex-center($justify: center, $dir: row) {
  display: flex;
  flex-direction: $dir;
  align-items: center;
  justify-content: $justify;
}

.grid {
  padding-left: 2em;
  display: grid;
  grid-template-columns: 10em auto;
  grid-template-rows: 10em 11em 8em 16em;

  h1 {
    margin-left: 1.5em;
    align-self: center;
    // justify-self: center;
    font-family: "Source Serif Pro", serif;
    font-weight: 300;
    grid-row: 1 / 2;
    grid-column: 1 / 3;
    z-index: 2;
  }
}

.content {
  grid-row: 1 / -1;
  grid-column: 1 / -1;
  position: relative;
  // width: 2em;
  // background: #ffbb7e;

  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 10em 10em 10em 10em 7em;
  --space: 7em;
  align-items: center;
  p {
    font-size: 0.9em;
    margin-left: 4em;
    // padding: 0em 3em;
    &:nth-child(1) {
      grid-row: 2 / 3;
    }
    &:nth-child(2) {
      grid-row: 4 / 5;
    }

    // &:nth-child(1) {
    //   outline: 1px solid black;
    //   margin-top: 9em;
    //   margin-bottom: var(--space);
    // }

    // &:nth-child(2) {
    //   outline: 1px solid black;
    //   // margin-bottom: 3em;
    //   margin-top: var(--space);
    // }
  }

  &::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    background: #ffbb7e;
    width: 2em;
    height: 100%;
  }
}

.img-container {
  align-self: center;
  grid-row: 3 / 4;
  grid-column: 1 / -1;
  z-index: 2;
  width: 18em;
}
</style>