<template>
  <section class="HelpSectionAppMaintenance__content">
      <div class="HelpSectionAppMaintenance__content-side-a">
        <slot name="title-side-a"></slot>
        <slot name="description-side-a"></slot>
      </div>
      <div class="HelpSectionAppMaintenance__content-side-b">
        <slot name="title-side-b"></slot>
        <slot name="description-side-b"></slot>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "@lkmx/flare/src/functions/_respond-to.scss";
.HelpSectionAppMaintenance__content {
  display: grid;
  gap: var(--f-gutter-xl);
  grid-auto-flow: column;
  grid-template-columns: 499px 499px;
    @include respond-to("<=m") {
      grid-template-columns: 1fr;
      grid-auto-flow: row;
      gap: var(--f-gutter);
  }
  .HelpSectionAppMaintenance__content-side-a, .HelpSectionAppMaintenance__content-side-b {
    display: grid;
    grid-template-rows: 20px 1fr;
    gap: var(--f-gutter); 
    padding: var(--f-gutter);  
    p {
      margin-bottom: 0;
    }
    p:first-child {
      font-family: var(--f-mono-text-font);
      color: var(--color-accent-pink);
      font-weight: var(--f-default-headers-weight);
      margin-bottom: 0;
      line-height: 20px;
    }
    p:last-child {
      color: var(--color-neutral-gray-01);
      height: 72px;
      @include respond-to("<=m") {
        height: auto;
      }
    }
  }
}
</style>