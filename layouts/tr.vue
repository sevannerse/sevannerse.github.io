<template>
  <div class="divide-y-2">
    <header class="container mx-auto flex flex-col py-5 max-w-2xl text-gray-600 body-font">
      <div class="flex flex-row justify-center relative">
        <div class="flex absolute top-0 right-0">
          <NuxtLink class="hover:text-gray-900 underline" :to="{ name: $route.name == 'index' ? 'lang' : $route.name, params: { lang: 'en' } }">en</NuxtLink>
          <NuxtLink class="ml-3 mr-3 sm:mr-0 hover:text-gray-900 underline" :to="{ name: $route.name == 'index' ? 'lang' : $route.name, params: { lang: 'hy' } }">hy</NuxtLink>
        </div>
        <NuxtLink :to="{ name: 'lang', params: { lang: 'tr' } }">
          <img src="/disk64.png"></img>
        </NuxtLink>
      </div>
      <div class="flex flex-col items-center mt-2 title-font font-medium">
        <NuxtLink class="flex text-gray-900 text-2xl" :to="{ name: 'lang', params: { lang: 'tr' } }">
          Sevan'ın Dlog'u
        </NuxtLink>
        <NuxtLink class="flex text-gray-600 text-base" :to="{ name: 'lang', params: { lang: 'tr' } }">
          Laravel
          <span class="text-gray-300">&nbsp;/&nbsp;</span>
          PHP
          <span class="text-gray-300">&nbsp;/&nbsp;</span>
          Javascript
        </NuxtLink>
      </div>
      <nav class="flex flex-row items-center text-base justify-center mt-5">
        <NuxtLink class="mx-3 hover:text-gray-900 underline" :to="{ name: 'lang', params: { lang: 'tr' } }">Dlog</NuxtLink>
        <NuxtLink class="mx-3 hover:text-gray-900 underline" :to="{ name: 'lang-about', params: { lang: 'tr' } }">Hakkımda</NuxtLink>
        <NuxtLink class="mx-3 hover:text-gray-900 underline" :to="{ name: 'lang-contact', params: { lang: 'tr' } }">İletişim</NuxtLink>
      </nav>
    </header>
    <div class="container mx-auto flex p-5 flex-col md:flex-row max-w-2xl">
      <Nuxt />
    </div>
  </div>
</template>