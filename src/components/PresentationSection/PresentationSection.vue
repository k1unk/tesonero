<template>
    <section class="presentation-block">
        <img class="presentation__main-img_mobile" src="@/assets/presentation-main-mobile.png" alt="">
        <div class="presentation-above-header__line_invisible"/>
        <div class="presentation-above-header__line"/>
        <h1 class="presentation__header">Lorem ipsum, dolor sit amet consectetur</h1>
        <div class="presentation-slider_mobile">
            <swiper
                class="swiper"
                :modules="modules"
                :slides-per-view="1"
                :space-between="10"
                :loop="true"
                :pagination="{ clickable: true }"
                :navigation="true"
            >
                <swiper-slide>
                    <div class="presentation-cluster__item presentation-cluster__item-1">
                        <img src="@/assets/presentation-cluster-item-2.svg" alt="">
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="presentation-cluster__item presentation-cluster__item-2">
                        <img src="@/assets/presentation-cluster-item-3.svg" alt="">
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="presentation-cluster__item presentation-cluster__item-3">
                        <img src="@/assets/presentation-cluster-item-1.svg" alt="">
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="presentation-cluster__item presentation-cluster__item-4">
                        <img src="@/assets/presentation-cluster-item-4.svg" alt="">
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="presentation-cluster__item presentation-cluster__item-5">
                        <img src="@/assets/presentation-cluster-item-2.svg" alt="">
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="presentation-cluster__item presentation-cluster__item-6">
                        <img src="@/assets/presentation-cluster-item-3.svg" alt="">
                        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
        <div class="presentation-cluster">
            <div class="presentation-cluster-line-1">
                <div class="presentation-cluster__item presentation-cluster__item-1">
                    <img src="@/assets/presentation-cluster-item-2.svg" alt="">
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                </div>
                <div class="presentation-cluster__item presentation-cluster__item-2">
                    <img src="@/assets/presentation-cluster-item-3.svg" alt="">
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                </div>
            </div>
            <div class="presentation-cluster-line-2">
                <div class="presentation-cluster__item presentation-cluster__item-3">
                    <img class="presentation-background-image-1"
                         src="@/assets/presentation-background-item-1.png"
                         alt=""
                    >
                    <img src="@/assets/presentation-cluster-item-1.svg" alt="">
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                </div>
                <img src="@/assets/presentation-main.png" alt="">
                <div class="presentation-cluster__item presentation-cluster__item-4">
                    <img class="presentation-background-image-2"
                         src="@/assets/presentation-background-item-2.png"
                         alt=""
                    >
                    <img src="@/assets/presentation-cluster-item-4.svg" alt="">
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                </div>
            </div>
            <div class="presentation-cluster-line-3">
                <div class="presentation-cluster__item presentation-cluster__item-5">
                    <img src="@/assets/presentation-cluster-item-2.svg" alt="">
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                </div>
                <div class="presentation-cluster__item presentation-cluster__item-6">
                    <img src="@/assets/presentation-cluster-item-3.svg" alt="">
                    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import {Pagination, Navigation} from 'swiper'
import {Swiper, SwiperSlide} from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/pagination'
import 'swiper/css/navigation'

export default {
    name: 'PresentationSection',
    components: {
        Swiper,
        SwiperSlide
    },

    setup() {
        return {
            modules: [Pagination, Navigation]
        };
    },
}
</script>

