<script setup>
import TheNavBar from '@/components/navbar/TheNavBar.vue'
import Button from 'primevue/button';
</script>

<template>
  <div class="flex justify-around items-center shadow-lg shadow-cyan-500/50">
    <div class="flex items-center gap-x-3">
      <div class="w-36">
        <img class="w-full h-auto" src="@/assets/logo.jpg" alt="logo.jpg"/>
      </div>
      <h1 class="text-2xl">CRC Notebook</h1>
    </div>
    <div class="justify-self-center">
      <TheNavBar/>
    </div>
    <div class="justify-self-center ">
      <Button label="Login" icon="pi pi-user" iconPos="left" class="p-button-success p-button-raised p-button-rounded" />
    </div>
  </div>
</template>
