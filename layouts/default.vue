<template>
  <div class="bg-white-200 px-2 py-2 md:px-5 md:py-5 box-border h-screen">
    <main
      class="flex flex-col bg-white-100 px-3 py-2 md:px-5 md:py-3 h-full mx-auto shadow-2xl xl:max-w-5xl rounded-md"
    >
      <header class="mb-2 md:mb-4">
        <nav class="flex flex-col md:flex-row">
          <div class="mx-auto md:mx-0">
            <NuxtLink id="logo_main" to="/">
              <img
                class="block mb-4 md:inline-block"
                style="height: 20px; width: 146px"
                height="20"
                width="146"
                src="~/assets/logo.svg"
                alt="Logo"
              />
            </NuxtLink>
          </div>
          <div class="mx-auto">
            <NuxtLink class="nav-link" to="/projects">Projecten</NuxtLink>
            <NuxtLink class="nav-link" to="/">Contact</NuxtLink>
            <NuxtLink class="nav-link" to="/">Blog</NuxtLink>
          </div>

          <div class="mx-auto mt-2 md:ml-auto md:mr-0 md:mt-0">
            <a class="icon-nav-link mr-2" href="https://github.com/Sanderdl">
              <svg
                role="img"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>GitHub</title>
                <path
                  d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"
                />
              </svg>
            </a>
            <a
              id="linkedin_icon"
              class="icon-nav-link"
              href="https://www.linkedin.com/in/sander-de-laat-654092b/"
            >
              <svg
                role="img"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <title>LinkedIn</title>
                <path
                  d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"
                />
              </svg>
            </a>
          </div>
        </nav>
      </header>
      <Nuxt tabindex="-1" class="grow overflow-y-auto" />
    </main>
  </div>
</template>

<style>
body {
  @apply text-gray-200;
}

.nav-link {
  @apply inline-block px-1 py-1 mx-1 uppercase text-xs font-semibold text-gray-200 border-b-2 border-white-100 box-border align-middle md:mx-5 md:px-3;
}

.nav-link:hover {
  @apply border-b-2 border-pink;
}

.nav-link:focus {
  outline-color: #e4038a;
}

.icon-nav-link {
  @apply inline-block box-content;

  height: 20px;
  width: 20px;
  fill: #37312d;
}

.icon-nav-link:hover {
  fill: #e4038a;
}

.icon-nav-link:focus {
  @apply bg-pink;

  outline-style: solid;
  outline-color: #e4038a;
}

h1 {
  @apply text-pink mt-3 md:mt-8;

  font-weight: bold;
  font-size: 2rem;
}

h2 {
  @apply text-2xl;

  font-weight: bold;
}
</style>
