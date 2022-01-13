<template>
  <div class="divide-y-2">
    <header class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center max-w-3xl text-gray-600 body-font">
      <NuxtLink class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0" :to="{ name: 'lang', params: { lang: 'tr' } }">
        <img src="/disk64.png"></img>
      </NuxtLink>
      <div class="flex flex-col">
        <NuxtLink class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0 ml-3 text-2xl" :to="{ name: 'lang', params: { lang: 'tr' } }">
          Sevan'ın Dlog'u
        </NuxtLink>
        <NuxtLink class="flex title-font font-medium items-center text-gray-600 mb-4 md:mb-0 ml-3 text-base" :to="{ name: 'lang', params: { lang: 'tr' } }">
          Laravel
          <span class="text-gray-300">&nbsp;/&nbsp;</span>
          PHP
          <span class="text-gray-300">&nbsp;/&nbsp;</span>
          Javascript
        </NuxtLink>
      </div>
      <nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
        <NuxtLink class="mr-8 hover:text-gray-900 underline" :to="{ name: 'lang', params: { lang: 'tr' } }">Dlog</NuxtLink>
        <NuxtLink class="mr-8 hover:text-gray-900 underline" :to="{ name: 'lang-about', params: { lang: 'tr' } }">Hakkımda</NuxtLink>
        <NuxtLink class="mr-8 hover:text-gray-900 underline" :to="{ name: 'lang-contact', params: { lang: 'tr' } }">İletişim</NuxtLink>
      </nav>
      <div class="flex flex-col">
        <NuxtLink class="hover:text-gray-900 underline" :to="{ name: $route.name, params: { lang: 'en' } }">en</NuxtLink>
        <NuxtLink class="hover:text-gray-900 underline" :to="{ name: $route.name, params: { lang: 'hy' } }">hy</NuxtLink>
      </div>
    </header>
    <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center max-w-3xl">
      <Nuxt />
    </div>
  </div>
</template>