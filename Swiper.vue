<template>
    <div class="swiper-container">
        <div class="swiper-wrapper" ref="swiperContainer">
            <slot />
        </div>
    </div>
</template>

<script>
import Swiper from 'swiper'

export default {
    name: 'swiper',
    props: {
        containerClass: {
            default: 'swiper-container'
        }
    },
    mounted() {
        new Swiper(`.${this.containerClass}`, {
            slidesPerView: 1,
        })
    }
}
</script>

<style>
.swiper-container {
    width: 100%;
    overflow: hidden;
}

.swiper-wrapper {
    white-space: nowrap;
}
</style>
