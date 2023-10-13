<script setup >
const props = defineProps({cardIndex:{type:Number}})
const text = ['Компания оказывает комплексные услуги по перевалке навалочных и насыпных грузов на рейдовом перегрузочном районе морского порта Кавказ по прямому варианту "борт-борт" с накоплением или без накопления груза, в том числе транспортно-экспедиционное обслуживание и агентирование судов. В номенклатуру обрабатываемых грузов входят зерновые грузы, уголь, железорудные концентраты, удобрения, окатыш.',
'Рейдовый перегрузочный район морского порта Кавказ позволяет обрабатывать морские суда дедвейтом до 100 000 тонн. Доставка груза осуществляется из мелководных портов России судами класса "река-море" дедвейтом от 3000 до 7000 тонн в каботажном плавании. Накопление груза осуществляется на балкере-накопителе дедвейтом 38264 тонны. Перевалка груза выполняется двумя кранами LIEBHERR FCC-CBG 25(30).Номинальная мощность перевалки до 15000 тонн/сутки.Компания владеет собственным флотом для осуществления каботажных перевозок.',
'Специалисты компании имеют большой стаж работы в морской индустрии и превосходную репутацию. Мы объединились в надежную, сильную и профессиональную команду, чтобы оказать нашим заказчикам безопасные и высококачественные услуги.',
'Наши клиенты - производители и экспортёры сырья, трейдеры сельскохозяйственной продукции, импортеры, энергетические компании и другие конечные пользователи. Грузовладельцам и фрахтователям мы обеспечиваем надежное обслуживание и гибкость.'
]
const img = Object.values(import.meta.glob('~/assets/image/*', {
  eager: true,
  import: 'default',
}))


</script>
<template>
    <div ref="main" class="h-full md:min-h-[60vh] min-h-[75vh]   justify-center items-center  flex md:py-[1rem] py-[2rem] flex-col relative w-screen ">
        <div class="video-bg shadow-xl w-screen h-screen">
            <video width="auto"  preload="auto" src="~assets/video-1.mp4" type="video/mp4" autoplay muted
                loop></video>
            <div class="effects"></div>
            <div class="video-bg__content ">

            </div>
        </div>
        <div class="md:w-[50%] min-h-fit w-[90%] flex flex-col gap-4 justify-center items-center md:h-[90%] mt-[1rem] md:mt-0">

          
            <CardComponent  v-if="props.cardIndex||props.cardIndex==0" :text="text[cardIndex]" :imagePath="img[cardIndex]" />
        
           
        </div>
    </div>
</template>
<style scoped>
.video-bg {
    /* min-height: 100%;
    width: 100%; */
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
    width: 100vw;
    height: 100vh;
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
    background-color: rgba(7, 7, 7, 0.3);
}



</style>