<template lang="pug">
div(class='h-screen flex-col p-2 text-slate-700 dark:text-white')
  div(class='p-2 hover:bg-gray-300 dark:hover:bg-dim-200 \
  rounded-full w-min' :class='defaultTransition')
    nuxt-link(to='/')
      div(class='w-8 h-8')
        IconLogo
  SidebarLeftTab(active)
    template(v-slot:icon)
      IconHome
    template(v-slot:name) Home
  SidebarLeftTab
    template(v-slot:icon)
      IconHashtag
    template(v-slot:name) Explore
  SidebarLeftTab
    template(v-slot:icon)
      IconInbox
    template(v-slot:name) Messages
  SidebarLeftTab
    template(v-slot:icon)
      IconBookmarks
    template(v-slot:name) Bookmarks
  SidebarLeftTab
    template(v-slot:icon)
      IconDocument
    template(v-slot:name) Lists
  SidebarLeftTab
    template(v-slot:icon)
      IconUser
    template(v-slot:name) Profile
  SidebarLeftTab
    template(v-slot:icon)
      IconBars
    template(v-slot:name) More
</template>

<script setup>
const { defaultTransition } = useTailwindConfig();
</script>
