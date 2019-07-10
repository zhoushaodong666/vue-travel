<template>
    <div class="wrapper">
    <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide><img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/1f69b3ab28f9962158c798a8a3f5b4b3.jpg_750x200_fb4bf7c4.jpg" alt=""></swiper-slide>
        <swiper-slide><img class="swiper-img" src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/a5d26ebec399b3aef013f45771ae96f0.jpg_750x200_de947eef.jpg" alt=""></swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
        
    </swiper>
    </div>
</template>

<script>
	export default {
		name: "HomeSwiper",
        data () {
	        return{
		        swiperOption:{}
            }
        }
	}
</script>

<style lang="stylus" scoped>
    .wrapper
        width:100%
        height :0

        .swiper-img
            width:100%
</style>