<template lang="pug">
div(:class='{"dark": darkMode}')
  div(class='bg-slate-200 dark:bg-dim-700 min-h-full')
    div(class='grid grid-cols-12 mx-auto px-6 lg:max-w-7xl \
    ')
      //- Left sidebar
      div(class='hidden md:block col-span-1 lg:col-span-2 \
      ') 
        div(class='sticky top-0')
          SidebarLeft
      //- Main content
      //- Right sidebar
</template>

<script setup>
const darkMode = ref(true);
</script>
