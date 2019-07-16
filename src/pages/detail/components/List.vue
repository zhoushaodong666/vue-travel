<template>
    <div>
        <div class="item" v-for="(item,index) of list" :key="index">
            <div class="item-title border-bottom">
                <span class="item-title-icon"></span>
                {{item.title}}
                <template v-if="item.price">
                    <div class="item-price">{{+item.price}}</div>
                    <div class="item-price-icon">￥</div>
                </template>
            </div>

            <div v-if="item.children" class="item-children">
                <detail-list :list="item.children"></detail-list>
            </div>
        </div>

    </div>
</template>

<script>
	export default {
		name: "DetailList",
		props: {
			list: Array
		}
	}
</script>

<style lang="stylus" scoped>
    .item-title-icon
        position: relative;
        left: .06rem
        top: .06rem
        display: inline-block;
        width: .36rem;
        height: .36rem;
        background: url(//s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat;
        margin-right: .1rem;
        background-size: .4rem 3rem;

    .item-title
        line-height: .8rem
        font-size: .32rem
        padding: 0 .2rem

    .item-children
        padding: 0 .2rem

    .item-price-icon
        float:right
        color: #ff9800
        font-size: .3rem

    .item-price
        float :right
        color: #ff9800
        font-size: .4rem

</style>