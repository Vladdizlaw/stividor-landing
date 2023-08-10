<script setup >
import { reactive, onMounted, ref, onBeforeUnmount } from 'vue'
const scroll = reactive({
    scrollPosition: 0
})
const main = ref(null)
const handleScroll = () => {
    if (process.client) {
        scroll.scrollPosition = window.scrollY
    }
}
onMounted(() => {
    if (process.client) {
        window.addEventListener("scroll", handleScroll);
      
    }
})
onBeforeUnmount(() => {
    if (process.client) {
        window.removeEventListener("scroll", handleScroll);
      
    }
})
const text = ['В Порту-Кавказ и в акватории Чёрного моря Компания оказывает такие услуги как рейдовая перевалка навалочных грузов.В номенклатуру обрабатываемых грузов входят уголь, ячмень, зерно, железорудные концентраты, удобрения, окатыш.Весь комплекс услуг компания оказывает по единой комплексной ставке которая включает перевалку, экспедирование, агентирование и т.д.',
'Наши клиенты, это производители и экспортёры сырья, трейдеры сельскохозяйственной продукции, импортеры, энергетические компании и другие индустриальные конечные пользователи. Грузовладельцам и фрахтователям мы обеспечиваем надежное обслуживание и гибкость.',
' Специалисты имеют большой стаж работы в морской индустрии. Они имеют превосходную репутацию, они объединилсиь в надежную, сильную и профессиональную команду, чтобы оказать для наших заказчиков безопасные и высококачественные услуги в областях, где это интересно клиентам.',
' Водная логистика Морской накопитель, емкостью 33000 тонн. Номинальная мощность перевалки 15000 тн/сутки. Организация сюрвейерского сопровождения. Догрузка флота, загруженного частично на другом терминале. Перевозка зерна на судах является оптимальным решением, когда речь идет о перемещении большого объема грузов на дальние расстояния'
]
const period =[250,550,950, 1250]
const img = Object.values(import.meta.glob('~/assets/image/*', {
  eager: true,
  import: 'default',
}))
const items ={text,img,period}
</script>
<template>
    <div ref="main" class="min-h-[250vh] md:min-h-[60vh] w-full justify-center items-center h-full flex py-[5rem] flex-col relative">
        <div class="video-bg shadow-xl max-w-[100%] ">
            <video width="auto" height="800" preload="auto" src="~assets/video-1.mp4" type="video/mp4" autoplay muted
                loop></video>
            <div class="effects"></div>
            <div class="video-bg__content ">

            </div>
        </div>
        <div class="md:w-[50%] w-[96%] flex flex-col gap-4 justify-center items-center fixed top-[10%]">

            
            <CardComponent v-for="value,index in items.text"  v-show="scroll.scrollPosition > items.period[index] && scroll.scrollPosition < (items.period[index+1]||1750)" :text="value" :imagePath="items.img[index]" :key="index"/>
            <!-- <CardComponent v-show="scroll.scrollPosition > 550&& scroll.scrollPosition < 950" :text="textForCardsList[1]" />
            <CardComponent v-show="scroll.scrollPosition > 950&& scroll.scrollPosition < 1250" :text="textForCardsList[2]" />
            <CardComponent v-show="scroll.scrollPosition > 1250" :text="textForCardsList[3]" /> -->
           
        </div>
    </div>
</template>
<style scoped>
.video-bg {
    min-height: 100%;
    width: 100%;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;

    /* min-width: 100%; */
    position: fixed;
    top: 0;
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

    transition: 1s opacity;
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



</style>