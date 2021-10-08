<template>
  <a class="btn-services" href="/">
    <h4><slot name="btn-services-title"></slot></h4>
    <p><slot name="btn-services-description"></slot></p>
    <slot name="btn-services-image"></slot>
  </a>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  @import "@lkmx/flare/src/functions/_respond-to.scss";
  #body-index {
    &__services-cubes {
      .btn-services {
        display: grid;
        gap: var(--f-gutter);
        text-decoration: none;
        p {
          margin-bottom: 0;
        }
        img {
          height: 32px;
        }
        h4 {
          color: var(--color-accent-pink);
          margin: 0;
          position: relative;
          letter-spacing: 0.5px;
          height: 52px;
        }
        p:nth-child(2) {
          color: var(--color-neutral-gray-01);
          margin: 0;   
        }
      }
    }
  }
</style>