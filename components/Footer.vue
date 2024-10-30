<template>
  <footer class="py-4">
    <div class="container mx-auto max-w-screen-md px-4">
      <div class="flex items-center justify-between gap-4 text-gray-500">
        <div class="dark:text-gray-300">
          © {{ new Date().getFullYear() }} Sarian. Created with ❤️ by
          <NuxtLink to="https://www.threads.net/@sakirsyarian" class="font-semibold" target="_blank">
            sakirsyarian
          </NuxtLink>
        </div>
        <div class="flex justify-center gap-2">
          <ThemeToggle/>
        </div>
      </div>
    </div>
  </footer>
</template>