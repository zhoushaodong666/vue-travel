<template>
    <div>
        <div class="banner" @click="handleBannerClick">
            <img class="banner-img"
                 src="//img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_600x330_b5e86902.jpg">
            <div class="banner-info">
                <div class="banner-title">长隆野生动物世界(AAAAA景区)</div>
                <div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span>39</div>
            </div>
        </div>
        <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
    </div>
</template>

<script>
	import CommonGallary from 'common/gallary/Gallary'

	export default {
		name: "DetailBanner",
        data (){
		    return {
			    showGallary:false,
			    imgs:[
				    'http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_r_800x800_ea3a0585.jpg',
				    'http://img1.qunarzz.com/sight/p0/1412/66/cd09ac9548221dcc4cef8dde5913c780.water.jpg_r_800x800_bea4d4a4.jpg'
			    ]
		    }
        },
        methods:{
	        handleBannerClick(){
                this.showGallary =true
            },
	        handleGallaryClose(){
		        this.showGallary =false
            }
        },
		components: {
			CommonGallary
		}
	}
</script>

<style lang="stylus" scoped>
    .banner
        position: relative
        overflow: hidden
        height: 0
        padding-bottom: 55%
        .banner-img
            width: 100%
        .banner-info
            display: flex
            position: absolute
            left: 0
            right: 0
            bottom: 0
            line-height: .6rem
            color: #fff
            background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
            .banner-title
                flex: 1
                font-size: .32rem
                padding: 0 .2rem
            .banner-number
                line-height: .32rem
                height: .32rem
                margin-top: .14rem
                padding: 0 .4rem
                border-radius: .2rem
                background: rgba(0, 0, 0, .8)
                font-size: .24rem
                .banner-icon
                    font-size: .24rem
                    padding-right: .1rem


</style>