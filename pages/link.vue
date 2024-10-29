<script setup>
useHead({
  title: 'Ahmad Sarian',
})

const links = [
  {
    title: "JavaScript for Beginners",
    // icon: Book,
    url: "https://jagojs.my.id/",
  },
  {
    title: "Follow me on Threads",
    // icon: AtSign,
    url: "https://threads.net/@sakirsyarian",
  },
  {
    title: "My Personal Website",
    // icon: Globe,
    url: "/",
  },
  {
    title: "Subscribe to my YouTube",
    // icon: Youtube,
    url: "https://youtube.com/@oterdev",
  },
  {
    title: "Buy me a Coffee",
    // icon: Coffee,
    url: "https://saweria.co/oterdev",
  },
];
const socials = [
  {
    name: "telegram",
    icon: "iconoir:telegram",
    url: "https://t.me/sakirsyarian",
  },
  {
    name: "instagram",
    icon: "iconoir:instagram",
    url: "https://instagram.com/sakirsyarian",
  },
  {
    name: "github",
    icon: "iconoir:github",
    url: "https://github.com/sakirsyarian",
  },
  {
    name: "email",
    icon: "iconoir:mail",
    url: "mailto:sariandeveloper@gmail.com",
  },
  {
    name: "tiktok",
    icon: "iconoir:tiktok",
    url: "https://tiktok.com/@oterdev",
  },
];
</script>

<template>
  <section class="flex min-h-screen items-center justify-center text-gray-500 dark:text-gray-300">
    <div class="container mx-auto max-w-md px-4 py-8">

      <header class="mb-8 text-center">
        <div class="mb-4 flex justify-center">
          <NuxtImg src="/profile.png" sizes="110px" class="rounded-full object-cover"/>
        </div>
        <h1 class="mb-2 text-2xl font-bold">Ahmad Sarian</h1>
        <p class="mb-4">
          Hi there! I like sharing simple tips and tricks with JavaScript to
          make your coding life easier.
        </p>
        <div class="flex items-center justify-center gap-4">
          <div v-for="social in socials" :key="social.name">
            <NuxtLink :to="social.url" target="_blank">
              <Icon :name="social.icon" size="25"/>
            </NuxtLink>
          </div>
        </div>
      </header>

      <main class="flex flex-col gap-4">
        <div v-for="link in links" :key="link.title">
          <NuxtLink :to="link.url" target="_blank"
                    class="block rounded-lg border p-4 transition-colors duration-200 hover:shadow-lg">
            <div class="flex items-center gap-3">
              <!-- <link.icon class="h-6 w-6" /> -->
              <span class="font-medium">{{ link.title }}</span>
            </div>
          </NuxtLink>
        </div>

      </main>

      <footer class="mt-8 text-center">
        <p class="text-sm">
          © {{ new Date().getFullYear() }} Sarian. Created with ❤️ by
          <NuxtLink to="https://github.com/sakirsyarian" target="_blank" class="font-semibold">
            sakirsyarian
          </NuxtLink>
        </p>
      </footer>

    </div>
  </section>
</template>