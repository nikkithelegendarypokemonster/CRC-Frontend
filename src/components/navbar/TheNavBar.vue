<script setup>
import { RouterLink, RouterView, useRoute } from "vue-router";
import {ref, computed} from 'vue'
const currentRoute = computed(() => {
  return useRoute().name
})
</script>

<template>
    <nav>
      <ul class="flex gap-x-14">
        <li>
          <RouterLink
          class="text-black p-2 hover:bg-sky-600 hover:text-white rounded"
          :class="{
            'text-sky-600 underline p-2 hover:bg-sky-600 hover:text-white rounded':currentRoute === 'home',
          }"
          to="/">Home</RouterLink>
        </li>
        <li>
          <RouterLink class="text-black p-2 hover:bg-sky-600  hover:text-white rounded"
          :class="{
            'text-sky-600 underline p-2 hover:bg-sky-600 hover:text-white rounded':currentRoute === 'activities',
          }"
          to="/activities">Activities</RouterLink>
        </li>
        <li>
          <RouterLink class="text-black p-2 hover:bg-sky-600  hover:text-white rounded"
          :class="{
            'text-sky-600 underline p-2 hover:bg-sky-600 hover:text-white rounded':currentRoute === 'announcements',
          }"
          to="/announce">Announcements</RouterLink>
        </li>
      </ul>
    </nav>
</template>
