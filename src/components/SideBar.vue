<template>
  <VNavigationDrawer expand-on-hover rail>
    <VList>
      <VListItem
        prepend-avatar="src/assets/my-avatar.jpeg"
        title="Elie BINGUE"
        subtitle="elie.b3@gmail.com"
      >
      </VListItem>
    </VList>
  <VDivider />

    <VList density="compact" nav>
      <VListItem
        prepend-icon="mdi-image"
        title="Black/White Gallery"
        value="color"
        color="grey"
        @click="selectOption(false)"
      />
      <VListItem
        prepend-icon="mdi-image"
        title="Color Gallery"
        value="color"
        color="blue-darken-2"
        @click="selectOption(true)"
      />
      </VList>
  </VNavigationDrawer>
</template>


<script setup lang="ts">
  // import { defineEmits } from 'vue';

  const emits = defineEmits(['selectOption'])

  const selectOption = (isColor: any) => {
    emits("selectOption", isColor)
  }
</script>



<style scoped lang="sass">


</style>
