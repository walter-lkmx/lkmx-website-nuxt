<template>
  <div class="services-cube-title">
    <slot name="title"></slot>
    <slot name="image">
      
    </slot>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  @import "@lkmx/flare/src/functions/_respond-to.scss";

  .services-cube-title {
    display: grid;
    grid-template-columns: 1fr auto;
    justify-content: space-around;
    grid-auto-flow: column;

    h4 {
      width: 85%;
    }
  }
</style>