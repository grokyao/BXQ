<template>
	<view>
	<uni-list>
	    <uni-list-item title="孙悟空" 
			note="肝阳上亢:高血压,红眼病"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="猪八戒" 
			note="痰湿阻滞:肥胖病"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>	
	<uni-list>
	    <uni-list-item title="沙和尚" 
			note="痰湿瘀滞:脱发"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>	
	<uni-list>
	    <uni-list-item title="红孩儿" 
			note="肝气郁结:自闭症"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>	
	
	</view>
</template>

<script>
	import uniList from '../../../components/uni-list/uni-list.vue'
	import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {

		},
		methods: {
		},
		components: {uniList,uniListItem}

	}
</script>

<style>

</style>
