<template>
  <q-layout view="lHh Lpr lFf">
    <div class="home-header flex justify-between items-center">
      <div>
        <router-link to="/" class="menu-item q-px-sm text-weight-medium">
          <img src="~src/assets/Site Images/logo.png" width="120">
        </router-link>
      </div>
      <div class="flex">
        <div class="menu">
          <router-link to="/" class="menu-item q-px-sm text-weight-medium">
            Home
          </router-link>
        </div>
        <div class="menu">
          <router-link to="/" class="menu-item q-px-sm text-weight-medium">
            Restaurants
          </router-link>
        </div>
        <div class="menu">
          <router-link to="/" class="menu-item q-px-sm text-weight-medium">
            Menu
          </router-link>
        </div>
        <div class="menu">
          <router-link to="/about-us" class="menu-item q-px-sm text-weight-medium">
            About Us
          </router-link>
        </div>
        <div class="menu">
          <router-link to="/contact-us" class="menu-item q-px-sm text-weight-medium">
            Contact Us
          </router-link>
        </div>
      </div>
      <div></div>
    </div>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

defineOptions({
  name: 'MainLayout'
})
const slide = ref(1);

const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
]

const leftDrawerOpen = ref(false)

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
