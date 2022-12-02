<template lang="pug">
nuxt-link(to='#' class='flex items-center p-3 pb-4 w-min hover:bg-gray-300 \
rounded-full dark:hover:bg-dim-200 \
h-12' :class='defaultTransition')
  div(class='w-6 h-6 text-dark')
    slot(name='icon')
  div(class='hidden ml-3 text-xl xl:block' :class="textClass")
    slot(name='name')
</template>

<script setup>
const { defaultTransition } = useTailwindConfig();
const props = defineProps({
  active: {
    type: Boolean,
    default: false,
  },
});
const textClass = computed(() =>
  props.active ? "font-semibold" : "font-normal"
);
</script>
