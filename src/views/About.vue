<template>
  <div class="about">
    <div class="icon">
      <i class="fas fa-wrench"></i>
    </div>
    <h1>Under construction</h1>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>


<style lang="scss">
@mixin flex-center($justify: center, $dir: row) {
  display: flex;
  flex-direction: $dir;
  align-items: center;
  justify-content: $justify;
}

.about {
  @include flex-center(center, column);
  // background: lightgreen;
  height: 90vh;

  h1 {
    text-align: center;
    padding: 1em 0 0 0;
  }
}

.fa-wrench {
  font-size: 7em;
}
</style>