<script setup>
const props=defineProps({
    text:String,
    imagePath:String,
})

</script>
<template>
    <div class="w-full h-full  rounded-md card overflow-hidden py-4 px-4 flex flex-col justify-center items-center gap-2">
        <div class="  w-full rounded-md flex justify-center">

           <img :src="props.imagePath" width="400" height="400"  class="rounded-md"/>
        </div>
        <div class="md:w-[80%] w-full title">
            <p  class="leading-[110%]  md:leading-[100%] text-[#ce8421] shadow_xl">{{ text }}</p>
    
        </div>
        </div>
</template>
<style scoped>
.card {
background: rgba( 60, 170, 182, 0.25 );
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 8.5px );
-webkit-backdrop-filter: blur( 8.5px );
border-radius: 10px;
border: 1px solid rgba( 255, 255, 255, 0.18 );
/* background:v-bind("props.imagePath") no-repeat left center fixed; */
}
.shadow_xl{
    filter: drop-shadow(-5px 6px 5px #000);
    }
.title{
    font-size: max(1vw,1rem)
}    
</style>
