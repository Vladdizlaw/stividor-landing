<script setup>
</script>
<template>
    <div class="w-full flex items-center justify-center flex-row gap-6 p-[1rem] h-fit relative overflow-hidden max-h-[25vh]  header">
       
        <!-- <div class="ocean1 z-[-1]">
  <div class="wave"></div>
  <div class="wave"></div>
</div> -->
       
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
.ocean1 { 
  height: 5%;
  width:100%;
  position:absolute;
  left:0;
  top:0;
  background: #015871;
  transform:rotate(180deg);
}

.wave {
  background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave.svg) repeat-x; 
  position: absolute;
  top: -198px;
  width: 6400px;
  height: 198px;
  animation: wave1 12s cubic-bezier( 0.36, 0.45, 0.63, 0.53) infinite;
  transform: translate3d(0, 0, 0);
}

.wave:nth-of-type(2) {
  top: -175px;
  animation: wave1 12s cubic-bezier( 0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
  opacity: 1;
}

@keyframes wave1 {
  0% {
    margin-left: 0;
  }
  100% {
    margin-left: -1600px;
  }
}

@keyframes swell {
  0%, 100% {
    transform: translate3d(0,-25px,0);
  }
  50% {
    transform: translate3d(0,5px,0);
  }
}
</style>