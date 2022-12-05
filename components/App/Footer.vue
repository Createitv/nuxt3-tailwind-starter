<script lang="ts" setup>
const route = useRoute()
const isHome = computed(() => route.path === '/')
</script>

<template>
  <footer
    :class="isHome ? 'bg-blue-700 text-white' : 'mt-10 text-black'"
    class="px-4 sm:px-0"
  >
    <div
      :class="isHome ? '' : 'border-t'"
      class="container py-4 mx-auto flex flex-col sm:flex-row justify-between gap-2 sm:items-center"
    >
      <NuxtLink
        :class="isHome ? 'text-white' : 'text-gray-800'"
        class="font-semibold text-lg"
        to="/"
      >
        <!-- <img
          loading="lazy"
          src="/logo.svg"
          alt="Logo"
          class="max-w-full h-10"
        /> -->
        {{ $t('app_name') }}
      </NuxtLink>
      <div class="text-sm">
        {{ $t('app_name') }} by
        <a
          :class="isHome ? 'text-white' : 'text-gray-800'"
          class="font-semibold"
          href="https://github.com/createitv"
        >
          彷`徨`
        </a>
        . All rights reserved
      </div>
    </div>
  </footer>
</template>
