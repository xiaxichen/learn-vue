<template>
    <div class="wrapper">
        <swiper :options="swiperOptions">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img"
                     :src="item.url"
                     alt="">
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
// es6写法
export default {
    name: 'HomeSwiper',
    data () {
        return {
            swiperOptions: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
                id: '0001',
                url: 'https://imgs.qunarzz.com/vs_ceph_vcimg/c0a60fa20379efa4f02ce527a680dc1b.jpeg'
            }, {
                id: '0002',
                url: 'https://imgs.qunarzz.com/vs_ceph_vcimg/b8c4527c41649814cc4cf86880abba54.jpeg'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
//因为 scoped 属性不会使当前样式影响到其他组件样式 所以需要属性穿透 即 >>>
//because scoped class will not let the current css style affect the style of other components. So need style penetration l.e >>>
.wrapper >>> .swiper-pagination-bullet-active
    background white

.wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    background #eee

    .swiper-img
        width 100%
</style>
