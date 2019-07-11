<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img"
                     :src="item.imgUrl"/>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-price">{{item.price}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
	export default {
		name: "HomeRecommend",
		data() {
			return{
				recommendList:[{
					id: "0001",
					imgUrl: "http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg",
					title: "长隆野生动物世界",
					price: 266,
				},
					{
						id: "0002",
						imgUrl: "http://img1.qunarzz.com/sight/p0/1707/88/889ae02b07140066a3.img.jpg_200x200_d3b1427c.jpg",
						title: "长隆欢乐世界",
						price: 239,
					},
					{
						id: "0003",
						imgUrl: "http://img1.qunarzz.com/sight/p0/1511/89/894fa87d78ab240890.water.jpg_200x200_9eb09344.jpg",
						title: "锦绣香江温泉城",price: 99,

					},
				]
            }
		}

	}
</script>

<style lang="stylus" scoped>
    @import "~styles/mixins.styl"
    .title
        line-height: .8rem
        background: #eee
        text-indent: .2rem

    .item
        display: flex
        height: 1.9rem
        .item-img
            width: 1.7rem
            height: 1.7rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width: 0
            .item-title
                line-height: .54rem
                font-size: .32rem
                ellopsis()
            .item-price
                float: left
                font-size: .4rem
                line-height: .4rem
                margin-top: .6rem
                color: #ff8300
            .item-button
                line-height: .44rem
                background: #ff8300
                margin-top: .6rem
                padding: 0 .2rem
                border-radius: .06rem
                float: right
                color: #fff
</style>