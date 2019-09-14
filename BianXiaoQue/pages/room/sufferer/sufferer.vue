<template>
	<view>
		<uni-list>
		    <uni-list-item title="牛魔王,男,58岁" 
				note="就诊日期:2019-1-22"
				showBadge="true" 
		        show-extra-icon="true" 
		        :extra-icon="{color: '#FD962E',size: '60',type: 'contact'}"
				v-on:click="gotoIndex()">
		    </uni-list-item>
		</uni-list>	
	</view>
</template>

<script>
	import uniList from '.../../../components/uni-list/uni-list.vue'
	import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			//页面跳转
			gotoIndex(){
				uni.navigateTo({
				url: ''
				});
			},
		},
		components: {
			uniList,uniListItem
		}
	}
</script>

<style>

</style>
