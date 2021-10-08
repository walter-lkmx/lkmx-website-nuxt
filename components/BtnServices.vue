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
        &:hover {
          h4 {
            color: var(--color-accent-blue-01);
          }
          img {
            border-block-end: 1px solid var(--color-accent-blue-01);
          }
        }
        p {
          margin-bottom: 0;
          color: var(--color-neutral-gray-01);
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
      }
    }
  }
</style>