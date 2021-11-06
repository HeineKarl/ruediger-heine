<template>
  <div class="blog">
    <div class="icon">
      <i class="fas fa-wrench"></i>
    </div>
    <h1>This is Blog coming soon!</h1>
  </div>
</template>

<script>
export default {
  name: "Blog",
};
</script>

<style lang="scss">
@mixin flex-center($justify: center, $dir: row) {
  display: flex;
  flex-direction: $dir;
  align-items: center;
  justify-content: $justify;
}

.blog {
  @include flex-center(center, column);
  // background: pink;
  height: 90vh;

  h1 {
    padding: 1em 0 0 0;
  }
}

.fa-wrench {
  font-size: 7em;
}
</style>