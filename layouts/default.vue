<template>
<header class="text-gray-600 body-font">
  <div
    class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"
  >
    <a
      class="flex title-font font-medium items-center text-green-900 mb-4 md:mb-0"
    >
      <img src="/nuxt.png" alt="nuxt logo" class="w-8" />
      <span class="ml-3 text-xl">Nuxt 3 beta</span>
    </a>
    <nav
      class="md:mr-auto md:ml-4 md:py-1 md:pl-4 md:border-l md:border-gray-400 flex flex-wrap items-center text-base justify-center"
    >
      <NuxtLink to="/" class="mr-5 hover:text-green-400"> Home</NuxtLink>
      <NuxtLink to="/about" class="mr-5 hover:text-green-400"> About</NuxtLink>
      <a href="https://v3.nuxtjs.org/docs/" class="mr-5 hover:text-green-400">Docs</a>
      <a href="https://github.com/nuxt/framework" class="mr-5 hover:text-green-400">Github</a>
    </nav>
  </div>
</header>
<div
  class="container w-full p-20 m-4 mx-auto my-16 text-center bg-white border-2 border-gray-300 border-dashed h-96 rounded-xl"
>

        <slot/>
</div>  
</template>
