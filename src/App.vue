<script setup lang="ts">
import SideBar from "./components/SideBar.vue";
import ImageGallery from './components/ImageGallery.vue';
import { ref } from 'vue';

const isWithColor = ref(true)

const onSelectOption = (isColor: boolean) => {
  isWithColor.value = isColor;
}
</script>

<template>
  <VApp>
    <SideBar @selectOption="onSelectOption"/>
    <VMain>
      <ImageGallery :isWithColor="isWithColor"/>
    </VMain>
  </VApp>
</template>
