<template>
  <article :class="`${page.title.toLowerCase().trim()}`">
    <nuxt-content :document="page" />
  </article>
</template>

<script>
export default {
  async asyncData({$content, params, error}) {
    const slug = params.slug || 'index';
    const page = await $content(slug).fetch().catch(err => {
      error({ statusCode: 404, message: 'Page not found'});
    });
    return {
      page
    };
  }
}
// export default {
//   async asyncData ({ $content }) {
//     const page = await $content('test').fetch()

//     return {
//       page
//     }
//   }
// }
</script>