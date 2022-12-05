<script lang="ts" setup>
const isOpen = ref(false)

const menus = ref([
  {
    text: 'menu_home',
    to: '/',
  },
  {
    text: 'menu_store',
    to: '/store',
  },
  {
    text: 'menu_blog',
    to: '/blog',
  },
  {
    text: 'menu_playground',
    to: '/playground',
  },
  {
    text: 'menu_dashboard',
    to: '/dashboard',
  },
])
</script>

<template>
  <header
    class="
      navbar-default
      bg-skin-fill
      text-skin-base
      py-3
      border-b
      sticky
      top-0
    "
  >
    <div
      class="
        container
        mx-auto
        pl-4
        pr-2
        sm:px-0
        flex flex-row
        items-center
        gap-4
        justify-between
      "
    >
      <NuxtLink class="font-bold text-skin-muted text-lg" to="/">
        {{ $t('app_name') }}
      </NuxtLink>
      <button
        aria-label="Menu"
        class="appearance-none px-2 py-2 rounded sm:hidden"
        type="button"
        @click="isOpen = !isOpen"
      >
        <Icon class="w-6 h-6" name="ri:menu-line" />
      </button>
      <div
        :class="
          isOpen
            ? 'fixed sm:relative top-16 shadow sm:shadow-none left-4 right-4 rounded-lg overflow-hidden bg-white sm:bg-transparent py-2'
            : 'hidden sm:flex sm:w-6/12'
        "
      >
        <nav
          class="
            flex flex-col
            sm:relative
            w-full
            items-start
            sm:flex-row
            sm:justify-end
            sm:gap-1
            sm:items-center
          "
        >
          <NuxtLink
            v-for="menu in menus"
            :key="menu.text"
            :to="menu.to"
            class="
              px-4
              py-2
              rounded-full
              w-full
              sm:w-auto
              text-skin-base
              hover:text-skin-hover
              hover:bg-skin-fill-hover
              transition
              duration-200
              font-medium
            "
            exact-active-class="bg-skin-fill-active text-skin-active"
          >
            {{ $t(menu.text) }}
          </NuxtLink>

          <div>
            <AppLangSwitcher
              class="
                text-skin-base
                hover:bg-skin-fill-hover
                hover:text-skin-hover
              "
            />
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<style scoped>
.navbar-default {
  --color-fill-active: #1d4ed8;
  --color-fill-hover: #1d4ed8;
  --color-text-active: #ffffff;
  --color-text-base: #484848;
  --color-text-hover: #ffffff;
  --color-text-muted: #1d4ed8;
}
</style>
