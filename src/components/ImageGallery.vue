<script lang="ts" setup>
  const p = defineProps(["isWithColor"]);
  const copyUrl = async (url:string) =>{
    await navigator.clipboard.writeText(url);
  }
</script>
<template>
  <VCard class="mx-5 my-2 pa-3">
    <VRow>
      <VCol 
        v-for="n in 432" 
        cols="4" 
        sm="3"
        md="2"
        lg="1"
        :key="n">
        <VCard
          @click="copyUrl(`https://picsum.photos/500/300?image=${n * 2 + 10}${p.isWithColor ? '' : '&grayscale'}`)">
          <VImg 
            :src="`https://picsum.photos/500/300?image=${n * 2 + 10}${p.isWithColor ? '' : '&grayscale'}`" 
            aspect-ratio="1" 
            cover 
            :lazy-src="`https://picsum.photos/10/6?image=${n * 2 + 10}${p.isWithColor ? '' : '&grayscale'}`">
            <template v-slot:placeholder>
              <VRow class="fill-height ma-0" align="center" justify="center">
                <VProgressCircular indeterminate color="grey-lighten-5"></VProgressCircular>
              </VRow>
            </template>
          </VImg>
        </VCard>
      </VCol>
    </VRow>
</VCard>
</template>