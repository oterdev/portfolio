<script setup lang="ts">
useHead({
  title: 'Ahmad Sarian',
})

const posts = [
  {id: 1, title: "Understanding React Hooks", date: "2023-06-15", views: 1200},
  {id: 2, title: "Mastering JavaScript", date: "2023-07-02", views: 980},
  {id: 3, title: "Next.js App Router Deep Dive", date: "2023-07-20", views: 1500},
];
const socials = [
  {
    name: "threads",
    href: "https://www.threads.net/@sakirsyarian",
  },
  {
    name: "instagram",
    href: "https://www.instagram.com/sakirsyarian/",
  },
];

const formatDate = (date: Date | string) => {
  return new Date(date).toLocaleDateString("id-ID", {
    year: "numeric",
    month: "numeric",
    day: "numeric",
  })
}
</script>

<template>
  <section class="py-10">
    <div class="container mx-auto max-w-screen-md px-4">
      <h1 class="mb-6 text-2xl font-semibold">
        Hi, I&apos;m <span class="text-blue-400">Sarian</span> 👋🏻
      </h1>
      <p class="mb-4">
        A fullstack dev who enjoys building cool, functional web apps
        using JavaScript and its ecosystem. Whether it is working on the
        frontend or backend, I&apos;m all about creating solutions that work
        and great.
      </p>
      <p>
        When I&apos;m not coding, I&apos;m usually sharing tips and tricks
        with the community through content creation. My goal is to help others
        learn and grow, while constantly improving my own skills.
      </p>
    </div>
  </section>

  <section class="py-10">
    <div class="container mx-auto max-w-screen-md px-4">
      <div class="flex items-center justify-between">
        <h2 class="mb-6 text-xl font-semibold">Latest posts</h2>
        <NuxtLink to="/blog" class="text-link">
          See all posts
        </NuxtLink>
      </div>
      <div class="grid grid-cols-1 gap-6">

        <ContentList path="/blog" v-slot="{ list }">
          <article v-for="post in list" :key="post._path" class="rounded-lg border transition-shadow hover:shadow-lg">
            <NuxtLink :to="post._path">
              <div class="p-6">
                <h3 class="mb-2 text-lg font-medium">{{ post.title }}</h3>
                <p>{{ post.description }}</p>
              </div>
            </NuxtLink>
          </article>
        </ContentList>

      </div>
    </div>
  </section>

  <section class="py-10">
    <div class="container mx-auto max-w-screen-md px-4">
      <h2 class="mb-6 text-xl font-semibold">Let&apos;s connect</h2>
      <p class="mb-6">
        If you want to get in touch with me about something or just to say hi,
        reach out on social media or send me an email.
      </p>
      <div class="space-y-4">
        <ul class="flex flex-wrap gap-2">
          <li v-for="social in socials" :key="social.name" class="flex items-center gap-2">
            <NuxtLink :to="social.href" class="text-link">
              {{ social.name }}
            </NuxtLink>
            /
          </li>
          <li class="line-clamp-1">
            <NuxtLink to="mailto:sariandeveloper@gmail.com" class="text-link">
              gmail
            </NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
