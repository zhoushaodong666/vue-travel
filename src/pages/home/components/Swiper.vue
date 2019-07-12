<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl">
            </swiper-slide>

            <div class="swiper-pagination" slot="pagination"></div>

        </swiper>
    </div>
</template>

<script>
	export default {
		name: "HomeSwiper",
		data() {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
                    loop:true,
					autoplay:4000
				},
				swiperList: [
					{
						id: "0001",
						imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/1f69b3ab28f9962158c798a8a3f5b4b3.jpg_750x200_fb4bf7c4.jpg",
					},
                    {
						id: "0002",
	                    imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/a5d26ebec399b3aef013f45771ae96f0.jpg_750x200_de947eef.jpg",
					},
				]
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