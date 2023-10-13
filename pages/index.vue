<script setup>
import { ref } from 'vue'
const cardIndex = ref(null)
const onCardSelect = (index) => {
  if (cardIndex.value == index) {
    cardIndex.value = null
  } else {
    cardIndex.value = index
  }

}
</script>
<template>
  <div class="page flex justify-start w-full md:h-screen h-fit flex-col overflow-hidden">
    <Header @card-select="onCardSelect" />
    <MainComponent :card-index="cardIndex" />
    <Footer />
  </div>
</template>
<style scoped>
.page {
  font-family: Finlandica;
}
</style>