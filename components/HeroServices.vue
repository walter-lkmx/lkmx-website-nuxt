<template>
  <section class="hero-services">
    <div class="hero-services__content">
      
      <div class="hero-services__side-a">
        <slot name="side-a"></slot>
      </div>
      <div class="hero-services__side-b">
        <slot name="side-b"></slot>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";
#body-services {
  overflow: hidden;
}

#body-index {
  &__hero-services {
    background: var(--f-header-background-color);
    height: 502px;
    display: grid;
    align-items: center;
    .content {
      .box {
        padding: 0;
      }
    }
  }
}

.hero-services {
  &__content {
    display: grid;
    grid-template-columns: 1fr 1fr;

    @include respond-to("<=m") { 
      grid-template-columns: 1fr;
      grid-template-rows: 244px 1fr;
    }
  }
  &__side-a {
    position: relative;
    z-index: 1;
    p {
      margin: 0;
    }
    img {
      max-width: unset !important;
      width: auto;
      height: 674px;
      z-index: 2;
      position: absolute;
      right: -420px;
      top: -119px;
      @include respond-to("<=m") {
        height: 300px;
        /* right: 0; */
        left: 30px;
        top: -35px;
        @include respond-to("<=xs") {
          height: 264px;
          right: -228px;
          top: 20px;
          left: unset;
        }
      }
    }
  }
  &__side-b {
    display: grid;
    gap: 12px;
    align-self: center;
    z-index: 2;
    @include respond-to("<=m") {
      padding: 0 var(--f-gutter) var(--f-gutter-xl) var(--f-gutter); 
      justify-self: end;
      p:last-child {
        font-size: var(--f-default-text-size);
        line-height: var(--f-paragraph-line-height);
        max-width: 97%;
      }
    }
    p:first-child {
      font-size: var(--f-default-text-size);
      line-height: 20px;
      color: var(--color-accent-cyan);
    }
    h1 {
      font-weight: var(--f-h2-text-weight);
      color: var(--color-accent-pink);
      line-height: 77px;
      letter-spacing: var(--f-h1-letter-space);
      margin-bottom: 0;
    }
    p {
      font-size: var(--f-h3-text-size);
      line-height: var(--f-h3-line-height);
      color: var(--color-neutral-gray-04);
      margin-bottom: 0;
      @include respond-to(">=xl") {
        max-width: 80%;
      }
    }
  }
}

</style>