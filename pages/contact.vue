<template>
  <main lang="nl">
    <section id="main_content">
      <h1>Contact</h1>
      <p>Ik ben op het momenteel niet opzoek naar een andere baan!</p>
      <form class="pt-8 w-full max-w-2xl" netlify>
        <label for="name">Naam</label>
        <input
          id="name"
          name="name"
          class="input-text mt-2 mb-4 p-2 h-8 w-full rounded bg-white-200 dark:bg-white-200 dark:text-gray-200"
          type="text"
        />
        <label for="email">Email</label>
        <input
          id="email"
          name="email"
          class="input-text mt-2 mb-4 p-2 h-8 w-full rounded bg-white-200 dark:bg-white-200 dark:text-gray-200"
          type="text"
        />
        <label for="message">Bericht</label>
        <textarea
          id="message"
          name="message"
          class="input-text mt-2 p-2 w-full rounded resize-none bg-white-200 dark:bg-white-200 dark:text-gray-200"
          style="height: 250px"
          cols="30"
          rows="10"
        ></textarea>
        <button class="contact-btn mt-4" type="submit">Neem contact op</button>
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

.contact-btn {
  @apply bg-pink text-white-100 py-1 px-2 rounded hover:bg-pink-light;
}
</style>
