<script lang="ts" setup>
//import {defineEmits} from "vue";

const emits = defineEmits(['selectOption']);
const selectOption = (isColor: boolean) =>{
  emits("selectOption", isColor)
}
</script>

<template>
  <VNavigationDrawer expand-on-hover rail>
    <VList>
      <VListItem prepend-avatar="https://randomuser.me/api/portraits/lego/1.jpg" title="Github Stuff"
        subtitle="randomstuff@gmailcom"></VListItem>
    </VList>
    <VList density="compact" nav>
      <VListItem prepend-icon="mdi-image" base-color="purple-darken-2" title="Color Gallery" value="color" @click="selectOption(true)"></VListItem>
      <VListItem prepend-icon="mdi-dialpad" title="Grayscale Gallery" value="gray" @click="selectOption(false)"></VListItem>
    </VList>

  </VNavigationDrawer>
</template>