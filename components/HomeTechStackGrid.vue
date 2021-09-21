<template>
  <section class="tech-stack-grid">
    <slot></slot>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";
@import "~/assets/sass/_general-functions";

.tech-stack-grid {
  max-width: 780px;
  p {
    @include grid($g:var(--f-gutter-xl), $gtc: repeat(10, 1fr));
    @include respond-to("<=m") {
      @include grid($g:var(--f-gutter), $gtc: repeat(5, 1fr));
    }
  }
}

</style>