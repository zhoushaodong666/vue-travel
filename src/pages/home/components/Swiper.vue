<template>
    <div class="wrapper">
        <swiper :options="swiperOption" v-if="showSwiper">
            <!-- slides -->
            <swiper-slide v-for="item of list" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl">
            </swiper-slide>

            <div class="swiper-pagination" slot="pagination"></div>

        </swiper>
    </div>
</template>

<script>
	export default {
		name: "HomeSwiper",
        props:{
			list:Array
        },
		data() {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
                    loop:true,
					autoplay:4000
				},

			}
		},
        computed:{
			showSwiper (){
				return this.list.length
            }
        }
	}
</script>

<style lang="stylus" scoped>
    // >>>样式穿透 使wrapper下的 swiper-pagination-bullet-active 的组件样式生效 不受scoped限制
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff

    .wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 26.67%
        background: #eee
        .swiper-img
            width: 100%
</style>