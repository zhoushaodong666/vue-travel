<template>
    <div>
        <detail-banner></detail-banner>
        <detail-header></detail-header>
        <div class="content">
            <detail-list :list="list"></detail-list>
        </div>
    </div>
</template>

<script>
	import DetailBanner from './components/Banner'
	import DetailHeader from './components/Header'
	import DetailList from './components/List'

	export default {
		name: "Detail",
		components: {
			DetailBanner,
			DetailHeader,
			DetailList,
		},
		data() {
			return {
				list: [{
					title: "成人票",
					children: [{
						title: "成人三馆联票",
						children: [{
							title: "成人三馆联票-上海店",
							price: 99.9
						}, {
							title: "成人三馆联票-北京店",
							price: 96.9
						}]
					}, {
						title: "成人五馆联票",
						children: [{
							title: "成人三馆联票-上海店",
							price: 139.9
						}, {
							title: "成人三馆联票-北京店",
							price: 136.9
						}]
					}]
				}, {
					title: "学生票",
					children: [{
						title: "学生三馆联票-上海店",
						price: 139.9
					}, {
						title: "学生三馆联票-北京店",
						price: 136.9
					}]
				}, {
					title: "儿童票",
					children: [{
						title: "儿童三馆联票-上海店",
						price: 139.9
					}, {
						title: "儿童三馆联票-北京店",
						price: 136.9
					}]
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped>
    .content
        height: 30rem
</style>