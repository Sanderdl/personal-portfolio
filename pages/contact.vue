<template>
  <main lang="nl">
    <section id="main_content">
      <h1>Contact</h1>
      <form class="pt-8 mx-auto w-full max-w-2xl" netlify>
        <label class="pb-2" for="name">Naam</label>
        <input
          id="name"
          name="name"
          class="input-text mt-2 p-2 h-8 w-full rounded bg-white-200 dark:bg-white-200"
          type="text"
        />
      </form>
    </section>
  </main>
</template>

<script>
export default {}
</script>

<style lang="postcss">
h1 {
  @apply text-pink mt-8;

  font-weight: bold;
  font-size: 2rem;
}

.input-text:focus,
.input-text:focus-visible {
  @apply border-pink border-2 outline-0;
}
</style>
