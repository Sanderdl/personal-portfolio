<template>
  <div
    class="relative inline-block w-10 mr-2 align-middle select-none transition duration-200 ease-in"
  >
    <input
      id="toggle"
      type="checkbox"
      name="toggle"
      class="bg-white-100 border-white-100 mr-1 focus:ring-transparent toggle-checkbox absolute block w-4 h-4 rounded-full appearance-none cursor-pointer"
      @change="toggleDarkMode"
    />
    <label
      for="toggle"
      class="toggle-label block h-6 -ml-1 -mt-1 rounded-full bg-pink cursor-pointer"
    ></label>
  </div>
</template>

<script>
export default {
  name: 'DarkModeToggle',
  data() {
    return {
      isDark: false,
    }
  },
  methods: {
    toggleDarkMode() {
      this.isDark = !this.isDark
      this.setDarkMode()
    },
    setDarkMode() {
      if (this.isDark) {
        document.documentElement.classList.add('dark')
      } else {
        document.documentElement.classList.remove('dark')
      }
    },
  },
}
</script>

<style>
.toggle-checkbox:checked {
  right: 0;
  border: none;
  background-color: rgb(129 124 214);
  background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' className='h-10 w-10' fill='%23FFF' viewBox='0 0 24 24' stroke='rgb(129 124 214)' > <path strokeLinecap='round' strokeLinejoin='round' d='M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z' /> </svg>");
}
.toggle-checkbox:checked + .toggle-label {
  background-color: rgb(76 73 188);
}
</style>
