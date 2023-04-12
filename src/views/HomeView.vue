<template>
    <div class="home">
        <HeaderCompnent />

        <section class="hero-section">
            <carousel :items-to-show="1" :autoplay="3000" :wrap-around="true">
                <slide v-for="slide in 3" :key="slide">
                    <div class="single-hero-items set-bg" style="background-image: url('/img/hero-1.jpg')">
                        <div class="container">
                            <div class="row banner-info">
                                <div class="col-lg-5">
                                    <span>Bag,kids</span>
                                    <h1>Black friday</h1>
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
                                        incididunt ut labore et dolore
                                    </p>
                                    <a href="#" class="primary-btn">Shop Now</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </slide>

                <template #addons>
                    <navigation />
                    <pagination />
                </template>
            </carousel>
        </section>

        <section class="women-banner spad">
            <div class="container-fluid">
                <div class="row">
                    <div class="col-lg-12 mt-5">
                        <carousel v-bind="settings" :breakpoints="breakpoints" :autoplay="2000" :wrap-around="true">
                            <slide v-for="slide in 6" :key="slide">
                                <div class="product-item">
                                    <div class="pi-pic">
                                        <img src="img/mickey1.jpg" alt="" />
                                        <ul>
                                            <li class="w-icon active">
                                                <a href="#"><i class="icon_bag_alt"></i></a>
                                            </li>
                                            <li class="quick-view">
                                                <a href="product.html">+ Quick View</a>
                                            </li>
                                        </ul>
                                    </div>

                                    <div class="pi-text">
                                        <div class="catagory-name">Coat</div>
                                        <a href="#">
                                            <h5>Mickey Baggy</h5>
                                        </a>
                                        <div class="product-price">
                                            $14.00
                                            <span>$35.00</span>
                                        </div>
                                    </div>
                                </div>
                            </slide>

                            <template #addons>
                                <navigation />
                                <pagination />
                            </template>
                        </carousel>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
// @ is an alias to /src
import HeaderCompnent from '@/components/HeaderComponent.vue'

import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
    components: {
        HeaderCompnent,
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
    data: () => ({
        // carousel settings
        settings: {
            itemsToShow: 1,
            snapAlign: 'center',
        },
        // breakpoints are mobile first
        // any settings not specified will fallback to the carousel settings
        breakpoints: {
            // 700px and up
            700: {
                itemsToShow: 3.5,
                snapAlign: 'center',
            },
            // 1024 and up
            1024: {
                itemsToShow: 3,
                snapAlign: 'start',
            },
        },
    }),
}
</script>

<style>
.set-bg {
    width: 100%;
    height: 725px;

}

.banner-info {
    margin-top: 230px;
}
</style>
