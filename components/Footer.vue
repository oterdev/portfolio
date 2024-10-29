<template>
  <footer className="py-4">
    <div className="container mx-auto max-w-screen-md px-4">
      <div className="flex items-center justify-between gap-4 text-gray-500">
        <div className="text-sm dark:text-gray-300">
          © {{ new Date().getFullYear() }} Sarian. Created with ❤️ by
          <NuxtLink to="https://www.threads.net/@sakirsyarian" class="font-semibold" target="_blank">
            sakirsyarian
          </NuxtLink>
        </div>
        <!-- <div className="flex justify-center gap-2">dark mode</div> -->
      </div>
    </div>
  </footer>
</template>
<script setup lang="ts">
</script>