<script setup>
</script>
<template>
  <div class="w-full h-full p-4 h-[15vh] relative overflow-hidden footer">
   
    <div class="w-full z-[100] flex text-black  shadow_xl flex md:justify-around flex-col md:flex-row items-center ">
      <div class="flex w-full text-[max(1.8vw,1.5rem)] gap-2 items-center  justify-center">
        <svg class="flex" xmlns="http://www.w3.org/2000/svg" height="32" viewBox="0 -960 960 960" width="48">
          <path
            d="M795-120q-122 0-242.5-60T336-336q-96-96-156-216.5T120-795q0-19.286 12.857-32.143T165-840h140q13.611 0 24.306 9.5Q340-821 343-805l27 126q2 14-.5 25.5T359-634L259-533q56 93 125.5 162T542-254l95-98q10-11 23-15.5t26-1.5l119 26q15.312 3.375 25.156 15.188Q840-316 840-300v135q0 19.286-12.857 32.143T795-120ZM229-588l81-82-23-110H180q0 39 12 85.5T229-588Zm369 363q41 19 89 31t93 14v-107l-103-21-79 83ZM229-588Zm369 363Z" />
        </svg>
        <p>+7 988 669 68 17</p>
      </div>

      <div class="flex flex-row w-full text-[max(1.8vw,1.5rem)] gap-2 items-center justify-center">
        <svg class="flex mt-2" xmlns="http://www.w3.org/2000/svg" height="32" viewBox="0 -960 960 960" width="48">
          <path
            d="M140-160q-24 0-42-18t-18-42v-520q0-24 18-42t42-18h680q24 0 42 18t18 42v520q0 24-18 42t-42 18H140Zm340-302L140-685v465h680v-465L480-462Zm0-60 336-218H145l335 218ZM140-685v-55 520-465Z" />
        </svg>
        <p>info@blackseasc.ru</p>
      </div>

      <div class="flex w-full text-[max(1.8vw,1.3rem)] gap-2 items-center justify-center md:leading-[100%] ">
        <svg class="md:flex hidden" xmlns="http://www.w3.org/2000/svg" height="32" viewBox="0 -960 960 960" width="48">
          <path
            d="M697-623h60v-60h-60v60Zm0 171h60v-60h-60v60Zm0 170h60v-60h-60v60Zm-56 162v-60h219v-600H465v112l-60-42v-130h515v720H641Zm-601 0v-390l271-194 270 194v390H364v-201H258v201H40Zm60-60h98v-201h226v201h97v-299L311-630 100-478.578V-180Zm541-365ZM424-180v-201H198v201-201h226v201Z" />
        </svg>
        <p>Краснодар, ул.Одесская, 41 офис. 308</p>
      </div>
    </div>

  </div>
</template>
<style scoped>
@font-face {
    font-family: Oswald;
    src: local(Oswald),
     url("/assets/Oswald-Bold.ttf") format("truetype");
}
.shadow_xl{
  font-family: Oswald;
  filter: drop-shadow(-5px 6px 5px #db8310);
}

.footer{
	background: rgba( 60, 170, 182, 0.25 );
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 8.5px );
-webkit-backdrop-filter: blur( 8.5px );
border-radius: 10px;
border: 1px solid rgba( 255, 255, 255, 0.18 );
}

</style>