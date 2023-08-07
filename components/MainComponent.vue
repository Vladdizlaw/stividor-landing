<script setup >
</script>
<template>
    <div class="min-h-[50vh] max-h-fit w-full justify-center h-full flex py-[5rem]">
        <div class="video-bg shadow-xl max-w-[100%] min-h-[100vh]">
            <video width="auto" height="800" preload="auto" src="~assets/video-1.mp4" type="video/mp4" autoplay muted
                loop></video>
            <div class="effects"></div>
            <div class="video-bg__content ">
                <p class="leading-[100%] ">В Порту-Кавказ и в акватории Чёрного моря Компания оказывает такие услуги как рейдовая перевалка
                    навалочных грузов. В номенклатуру обрабатываемых грузов входят уголь, ячмень, зерно, железорудные
                    концентраты, удобрения, окатыш. Весь комплекс услуг компания оказывает по единой комплексной ставке
                    которая включает перевалку, экспедирование, агентирование и т.д.</p>
            </div>
        </div>

        
    </div>
</template>
<style scoped>
.video-bg {
    height: auto;
    width: 100%;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;

    /* min-width: 100%; */
    position: fixed;
    top:0;
    z-index: -999;
}

.video-bg video {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.effects {
    position: absolute;
    object-fit: cover;
    top: 0;
    left: 0;
    z-index: 2;
    width: 100%;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.3);
}

.video-bg__content {
    z-index: 2;
    color: #ffffff;
    font-size: 1.7rem;
    padding:1rem;
    height:100%;
    text-align: left;
    transition: 0.3s;
    opacity:0;
    cursor: pointer;
}
.video-bg__content:hover{
    opacity:0.9;
    
}
.main {
    max-width: 1600px;
    margin: 0 auto;
    margin-top: 50px;
    padding: 0 20px;
}</style>