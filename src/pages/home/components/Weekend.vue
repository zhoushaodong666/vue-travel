<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img"
                         :src="item.imgUrl"/>
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
	export default {
		name: "HomeWeekend",
		data() {
			return {
				recommendList: [{
					id: "0001",
					imgUrl: "http://img1.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg",
					title: "清远周边逛",
					desc: "人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？"
				},
					{
						id: "0002",
						imgUrl: "http://img1.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg",
						title: "浮在海上的绿洲",
						desc: "南国滨海之城，避寒胜地，有暖暖的阳光，海风习习，吃着海鲜逛逛老街多惬意啊"
					},
					{
						id: "0003",
						imgUrl: "http://img1.qunarzz.com/sight/source/1505/92/580e9ea4f37a1b.jpg_r_640x214_72112761.jpg",
						title: "广州必打卡",
						desc: "感受现代与传统相融合的广州"

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

    .item-img-wrapper
        overflow: hidden
        height: 0
        padding-bottom: 36.4%

    .item-img
        width: 100%

    .item-info
        padding: .1rem

        .item-title
            line-height: .54rem
            font-size: .32rem
            ellopsis()

        .item-desc
            line-height: .4rem
            color: #ccc
            ellopsis()

</style>