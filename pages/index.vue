<script setup>
import { onMounted } from 'vue';
onMounted(()=>{
  window.scrollTo(0,0)
})
</script>
<template>
    <div class="page flex justify-start w-full min-h-screen max-h-fit flex-col gap-6">
      <Header/>
      <MainComponent/>
      <Footer/>
    </div>
</template>
<style scoped>
.page {
    font-family: "Finlandica";
}
</style>