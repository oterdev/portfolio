<template>
  <section class="flex min-h-screen flex-col">
    <div class="text-gray-500 dark:text-gray-300">
      <Header/>
      <main class="flex-grow">
        <slot/>
      </main>
      <Footer/>
    </div>
  </section>
</template>