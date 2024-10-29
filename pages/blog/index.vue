<template>
  <div>
    <h1 class="mb-4">Blog Posts</h1>
    <div class="grid gap-4">
      <ContentList path="/blog" v-slot="{ list }">
        <article v-for="post in list" :key="post._path">
          <NuxtLink :to="post._path">
            <h2>{{ post.title }}</h2>
            <p>{{ post.description }}</p>
          </NuxtLink>
        </article>
      </ContentList>
    </div>
  </div>
</template>