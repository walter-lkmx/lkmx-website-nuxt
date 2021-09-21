<template>
  <section class="hero">
    <div class="hero__content">
      <div class="hero__side-a">
        <slot name="side-a"></slot>
      </div>
      <div class="hero__side-b">
        <slot name="side-b"></slot>
      </div>
    </div>
    <div class="hero__ribbon"></div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";

#body-index {
  &__hero {
    background: var(--color-neutral-black);
  }
}

.hero {
  &__content {
    padding: var(--f-gutter);
    display: grid;
    grid-template-columns: 1fr 1fr;
    @include respond-to("<=m") {
      grid-template-columns: 1fr;
    }
    max-height: 390px;
    @include respond-to("<=m") {
      max-height: 600px;
    }
    align-items: start;
    z-index: 2;
    position: relative;
  }
  &__side-a {
    padding-top: var(--f-gutter-xxl);
    @include respond-to("<=m") {
      padding-top: var(--f-gutter-l);
      text-align: center;
    }
    h1 {
      color: var(--color-accent-pink);
      @include respond-to("<=m") {
        font-size: var(--f-gutter-xl);
        line-height: 1;
      }
    }
    h3 {
      color: var(--color-accent-cyan);
    }
    p {
      width: 95%;
      color: var(--color-neutral-white);
    }
  }
  &__side-b {
    padding-top: var(--f-gutter-l);
    img {
      width: 580px;
      height: auto;
      object-fit: contain;
    }
  }
  &__ribbon {
    height: 104px;
    background: var(--color-accent-blue-01);
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 1;
  }
}
</style>
