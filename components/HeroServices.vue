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
    /* overflow: hidden; */
    .content {
      .box {
        padding: 0;
      }
    }
  }
}

.hero-services {
  /* overflow: hidden; */
  &__content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    z-index: 2;
    position: relative;
  }
  &__side-a {
    position: relative;
    p {
      margin: 0;
      position: relative;
    }
    img {
      max-width: unset !important;
      width: auto;
      height: 674px;
      z-index: 1;
      position: absolute;
      right: -501px;
      top: -162px;
      /* transform: translate(-680px, -130px); 
      @include respond-to("<=xl") {
        transform: translate(-425px, -120px); 
      } */

    }
  }
  &__side-b {
    display: grid;
    gap: 12px;
    align-self: center;
    z-index: 2;
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
      max-width: 80%;
    }
  }
}

</style>