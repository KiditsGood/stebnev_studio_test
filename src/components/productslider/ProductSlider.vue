<template>
    <div class="picture">
        <img src="../../assets/img/product2.png" alt="" class="picture__main">
        <p class="picture__model"><span class="picture__model-big">C</span>252</p>
    </div>
    <swiper
            class="slider"
            :slides-per-view="4"
            :space-between="30"
            :break-points="360"
            @swiper="onSwiper"
            @slideChange="onSlideChange"
    >
        <swiper-slide class="slider__item">
            <img src="../../assets/img/product1.png" alt="" class="slider__item-image">
        </swiper-slide>
        <swiper-slide class="slider__item active">
            <img src="../../assets/img/product2.png" alt="" class="slider__item-image">
        </swiper-slide>
        <swiper-slide class="slider__item">
            <img src="../../assets/img/product3.png" alt="" class="slider__item-image">
        </swiper-slide>
        <swiper-slide class="slider__item">
            <img src="../../assets/img/product4.png" alt="" class="slider__item-image">
        </swiper-slide>
        <swiper-slide class="slider__item">
            <img src="../../assets/img/product1.png" alt="" class="slider__item-image">
        </swiper-slide>
        <swiper-slide class="slider__item">
            <img src="../../assets/img/product2.png" alt="" class="slider__item-image">
        </swiper-slide>
        <swiper-slide class="slider__item">
            <img src="../../assets/img/product3.png" alt="" class="slider__item-image">
        </swiper-slide>
        <swiper-slide class="slider__item">
            <img src="../../assets/img/product4.png" alt="" class="slider__item-image">
        </swiper-slide>
    </swiper>
</template>

<script>
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import 'swiper/css';

    export default {
        name: "ProductSlider",

        components: {
            Swiper,
            SwiperSlide,
        },

        methods: {
            slideChanger() {
                const mainImage = document.querySelector('.picture__main')
                const sliderItem = document.querySelectorAll('.slider__item')

                sliderItem.forEach(el => {
                    el.addEventListener('click', function () {
                        mainImage.setAttribute('src', this.firstElementChild.src)

                        sliderItem.forEach(el => {
                            el.classList.remove('active')
                        })

                        this.classList.add('active')
                    })
                })
            }
        },

        mounted() {
            this.slideChanger()
        },

        setup() {
            const onSwiper = (swiper) => {
                console.log(swiper);
            };
            const onSlideChange = () => {
                console.log('slide change');
            };
            return {
                onSwiper,
                onSlideChange,
            };
        },
    }
</script>