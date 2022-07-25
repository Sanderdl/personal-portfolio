<template>
  <article>
    <nuxt-content :document="project" />
  </article>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const project = await $content('projects', params.slug).fetch()

    return { project }
  },
}
</script>

<style lang="postcss">
.nuxt-content h1 {
  @apply text-pink mt-8;

  font-weight: bold;
  font-size: 2rem;
}

.nuxt-content p {
  @apply mb-1 mt-8;
}
</style>
