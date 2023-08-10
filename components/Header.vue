<script setup>
const handleClick = (linkName)=>{

}
</script>
<template>
    <div class="w-full flex flex-col items-center justify-center flex-row gap-6 p-[1rem] md:h-[35vh] h-auto relative overflow-hidden   header select-none">
  
   <div  class="w-full flex items-center justify-center flex-row gap-6 h-full">   
        <div class="h-full  z-[10] w-[8rem] title">
            <img src="~assets/logo.svg" alt="">
        
        </div>
        <div class=" w-fit h-full">

            <h1 class="title  text-[#ce8421] drop-shadow-xl">
               ЧЕРНОМОРСКАЯ СТИВИДОРНАЯ КОМПАНИЯ 
            </h1>
            <h1 class="title_sm text-xl text-[#d6b659] drop-shadow-xl">
               Рейдовая перевалка грузов
            </h1>
        </div></div> 
        <div class="w-full flex justify-center gap-20 text-[#ce8421]  ">
          <p @click="handleClick('1')" class="cursor-pointer title_sm_sm">Услуги</p>
          <p @click="handleClick('2')" class="cursor-pointer title_sm_sm">Наши клиенты</p>
          <p @click="handleClick('3')" class="cursor-pointer title_sm_sm">Наши возможности</p>
          <p @click="handleClick('4')" class="cursor-pointer title_sm_sm">Логистика</p>
          <p></p>
        </div>
    </div>
</template>
<style scoped>
@font-face {
    font-family: Finlandica;
    src: local(Finlandica),
     url("/assets/Finlandica-Bold.ttf") format("truetype");
}
.header{
	background: rgba( 60, 170, 182, 0.25 );
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 8.5px );
-webkit-backdrop-filter: blur( 8.5px );
border-radius: 10px;
border: 1px solid rgba( 255, 255, 255, 0.18 );
}
.title{
	font-family: Finlandica;
	font-weight: 700;
	font-size:max(3vw,1.8rem);
	filter: drop-shadow(-5px 6px 5px #000);
	line-height: 100%;
	
}
.title_sm{
	font-size:max(2vw,1rem);
	filter: drop-shadow(-5px 6px 5px #000);
}
.title_sm_sm{
	font-size:max(1.5vw,0.8rem);
  transition:0.1s;
  filter: drop-shadow(-1px 2px 1px #131212);
  user-select: none;
}


.title_sm_sm:hover{
  filter: drop-shadow(-2px 3px 2px #000);
}
.title_sm_sm:active{
  transform: scale(0.9);
}



</style>