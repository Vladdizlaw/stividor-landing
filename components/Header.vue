<script setup>
import { ref, onMounted } from 'vue'
const emit = defineEmits(['card-select'])
const cardIndex = ref(null)
const cardValues = ['Услуги', 'Логистика', 'Наши возможности', 'Наши клиенты']
const handleClick = (linkName) => {
  cardIndex.value == linkName ? cardIndex.value = null : cardIndex.value = linkName
  emit('card-select', linkName)
}
onMounted(() => {
  // emit('card-select', cardIndex.value)
})
</script>
<template>
  <div
    class="w-full flex flex-col items-center justify-center flex-row gap-2 p-[1rem] md:h-[max(23vh,8rem)] h-fit relative    header select-none shrink-0 z-10 relative">

    <div class="w-full flex items-center justify-start flex-row gap-6  overflow-hidden">
      <div class="max-h-[80%] md:h-full  z-[10] w-[max(4vw,8rem)] md:w-[14vw] title flex md:ml-[2rem]">
        <img src="~assets/logo.svg" alt="">
      </div>
      <div class=" w-fit place-self-start place-items-center md:mt-6">

        <h1 class="title  text-[#ce8421] ">

          ЧЕРНОМОРСКАЯ СТИВИДОРНАЯ КОМПАНИЯ
        </h1>
        <h2 class="title_sm md:pl-10 text-xl text-[#d6b659] drop-shadow-xl">
          Рейдовая перевалка грузов
        </h2>
      </div>
    </div>
    <div
      class="w-full  md:justify-center md:gap-20  justify-around sm:gap-6 text-[#ce8421] flex absolute md:bottom-2 bottom-[-2rem] z-[100]">
      <p v-for="card, index in cardValues" :key="index" @click="handleClick(index)" class="cursor-pointer title_sm_sm "
        :class="{ 'active': cardIndex == index }">{{ card }}</p>
    </div>
  </div>
</template>
<style scoped>
@font-face {
  font-family: Finlandica;
  src: local(Finlandica),
    url("/assets/Finlandica-Bold.ttf") format("truetype");
}

.header {
  background: rgba(14, 108, 223, 0.25);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
  backdrop-filter: blur(8.5px);
  -webkit-backdrop-filter: blur(8.5px);
  border-radius: 0 0 10px 10px;
  border: 1px solid rgba(255, 255, 255, 0.18);
}

.active {
  color: rgb(248, 211, 29);
  filter: drop-shadow(-10px 6px 4px #000);
}

.title {
  font-family: Finlandica;
  font-weight: 700;
  font-size: max(3.7vw, 1.5rem);
  filter: drop-shadow(-5px 6px 5px #0a0a0a);
  line-height: 100%;

}

.title_sm {
  font-size: max(1.8vw, 1.1rem);
  filter: drop-shadow(-5px 6px 5px #222121);
}

.title_sm_sm {
  font-size: max(1.7vw, 0.8rem);
  transition: 0.1s;
  filter: drop-shadow(-1px 2px 1px #383535);
  user-select: none;
}


.title_sm_sm:hover {
  filter: drop-shadow(-2px 3px 2px #000);
}

.title_sm_sm:active {
  transform: scale(0.96);
}
</style>