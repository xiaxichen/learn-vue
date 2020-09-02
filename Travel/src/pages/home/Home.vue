<template>
    <div>
        <div>
            <home-header></home-header>
        </div>
        <div>
            <home-swiper></home-swiper>
        </div>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'

export default {
    name: 'Home',
    components: {
        HomeHeader,
        HomeSwiper
    }
}
</script>

<style>
.home {
    font-size: 20px;
}
</style>
