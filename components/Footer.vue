<script setup>
</script>
<template>
    <div class="w-full h-[30vh]  relative overflow-hidden">
      <div class="ocean">
  <div class="wave"></div>
  <div class="wave"></div>
</div>
        <!-- <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" class="svg">
            <path fill="#000b76" fill-opacity="1.3"
                d="M0,192L26.7,170.7C53.3,149,107,107,160,112C213.3,117,267,171,320,208C373.3,245,427,267,480,250.7C533.3,235,587,181,640,165.3C693.3,149,747,171,800,186.7C853.3,203,907,213,960,224C1013.3,235,1067,245,1120,229.3C1173.3,213,1227,171,1280,138.7C1333.3,107,1387,85,1413,74.7L1440,64L1440,320L1413.3,320C1386.7,320,1333,320,1280,320C1226.7,320,1173,320,1120,320C1066.7,320,1013,320,960,320C906.7,320,853,320,800,320C746.7,320,693,320,640,320C586.7,320,533,320,480,320C426.7,320,373,320,320,320C266.7,320,213,320,160,320C106.7,320,53,320,27,320L0,320Z"
                class="path"></path>
        </svg> -->
        
        <!-- <div class="ball"></div> -->
    
    
</div>
</template>
<style scoped>

.ocean { 
  height: 5%;
  width:100%;
  position:absolute;
  bottom:0;
  left:0;
  background: #015871;
  
}

.wave {
  background: url(https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave.svg) repeat-x; 
  position: absolute;
  top: -198px;
  width: 6400px;
  height: 198px;
  animation: wave 12s cubic-bezier( 0.36, 0.45, 0.63, 0.53) infinite;
  transform: translate3d(0, 0, 0);
}

.wave:nth-of-type(2) {
  top: -175px;
  animation: wave 12s cubic-bezier( 0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
  opacity: 1;
}

@keyframes wave {
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