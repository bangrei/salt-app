<template>
  <div class="our-wrapper">
    <div class="our-content">
        <div class="our-title">Our Specialty</div>
        <div class="out-subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc sit amet congue aliquam.</div>
        <div class="carousels">
            <carousel :items-to-show="slidesPerView - 0.5" :wrap-around="true" :transition="500">
                <slide v-for="(content, index) in contents" :key="index">
                    <img class="carousel-img img-ratio" :src="require('@/assets/' + content.image)"/>
                    <!-- <span>{{ content.title }}</span> -->
                </slide>
                <template #addons>
                    <pagination />
                </template>
            </carousel>
        </div>
    </div>
  </div>
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination } from 'vue3-carousel';
export default {
    name: 'OurSpecialty',
    components: {
        Carousel,
        Slide,
        Pagination,
    },
    data() {
        return {
            slidesPerView: 3,
            contents: [],
        }
    },
    created() {
        this.contents = [
            {
                title : "Accessories",
                image: "accessories.svg",
            },
            {
                title : "Speed",
                image: "speed.svg",
            },
            {
                title : "Exhaust",
                image: "exhaust.svg",
            },
        ]
    }
}
</script>

<style scoped>
    .our-wrapper {
        padding: 32px 7%;
        background: #509FDD;
    }
    .our-content {
        background: #FFF;
        padding: 16px;
    }
    .our-title {
        color: #029FE4;
        font-size: 24px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
        text-transform: uppercase;
        padding-bottom: 16px;
    }
    .our-subtitle {
        color: #303030;
        font-size: 14px;
        font-style: normal;
        font-weight: 300;
        line-height: 24px; /* 171.429% */
    }
    .carousels {
        padding: 32px 0;
        background: #FFF;
    }
</style>
