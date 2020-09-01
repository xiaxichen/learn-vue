<template>
    <div>
        <div>
            <home-header></home-header>
        </div>
        <div class="home">home</div>
        <router-link to="/list">列表页</router-link>
    </div>
</template>

<script>
import HomeHeader from './components/Header'

export default {
    name: 'Home',
    components: {
        HomeHeader
    }
}
</script>

<style>
.home {
    font-size: 20px;
}
</style>
