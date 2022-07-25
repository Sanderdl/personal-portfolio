<template>
  <div>
    <section class="text-center p-8">
      <h1 class="hidden">Over mij</h1>
      <header class="text-4xl title">Front end developer bij Innofaith</header>
      <p class="my-4 mb-8 bold-title">Mobile en web development</p>
      <img
        class="mx-auto rounded-full object-cover"
        src="~/assets/images/foto_sander.jpg"
        style="height: 139px"
        alt="Een foto van Sander de Laat"
        height="139"
        width="139"
        decoding="async"
      />
    </section>
    <section>
      <h2 class="bold-title mb-2 md:mb-6">Projecten</h2>
      <ul>
        <li v-for="(project, index) of projects" :key="project.slug">
          <article class="project-card">
            <picture class="project-img">
              <source :srcset="`${project.image}.webp`" type="image/webp" />
              <source :srcset="`${project.image}.jpg`" type="image/jpeg" />
              <img
                :src="`${project.image}.jpg`"
                :alt="`Thumbnail voor ${project.title}`"
                height="500"
                width="500"
                :loading="index > 2 ? 'lazy' : ''"
                decoding="async"
              />
            </picture>
            <div class="project-info">
              <header class="bold-title">{{ project.title }}</header>
              <p class="mb-4">{{ project.description }}</p>
              <div>
                <span v-for="tag of project.tags" :key="tag" class="tag">{{
                  tag
                }}</span>
              </div>
              <div class="mt-8">
                <NuxtLink :to="{ path: project.path }" class="project-link">
                  Bekijk project
                </NuxtLink>
              </div>
            </div>
          </article>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const projects = await $content('projects')
      .only(['title', 'description', 'image', 'slug', 'tags'])
      .sortBy('sortKey', 'asc')
      .fetch()

    return {
      projects,
    }
  },
}
</script>

<style lang="postcss">
.project-card {
  @apply relative w-full md:flex mb-6;
}

.project-img {
  @apply w-full md:w-1/2;
}

.project-info {
  @apply absolute text-sm p-3 text-gray-200 bg-gradient-to-b from-white-100 to-transparent top-0 left-0 right-0 md:bg-none md:relative md:w-1/2 md:px-6 md:py-0;
}

.tag {
  @apply p-2 m-1 bg-white-100 text-xs inline-block border-pink border text-pink rounded-2xl leading-3;
}

.tag:first-child {
  @apply ml-0;
}

.project-link {
  @apply bg-pink text-white-100 py-1 px-2 rounded hover:bg-pink-light;
}

.project-link:focus {
  @apply focus:opacity-50;

  outline: none;
}
</style>
