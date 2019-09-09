<template>
	<view>
		
	<uni-list>
	    <uni-list-item title="张仲景" 
			note="精究方术,上以疗君亲之疾……"
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#FD962E',size: '60',type: 'contact-filled'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="诊疗统计" 
			note="好评如潮"
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'flag'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="出诊地点" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'map'}">
	    </uni-list-item>
	</uni-list>	
	<uni-list>
	    <uni-list-item title="出诊时间" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'circle'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="钱包" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'locked'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="医案" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'list'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="常用方" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'bars'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="读书" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'eye'}">
	    </uni-list-item>
	</uni-list>
		
	<uni-list>
	    <uni-list-item title="考试与培训" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'loop'}">
	    </uni-list-item>
	</uni-list>
			
	<uni-list>
	    <uni-list-item title="医友" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'personadd'}">
	    </uni-list-item>
	</uni-list>		

	<uni-list>
	    <uni-list-item title="师徒" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'star'}">
	    </uni-list-item>
	</uni-list>	
			
	<uni-list>
	    <uni-list-item title="设置" 
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'gear'}">
	    </uni-list-item>
	</uni-list>				
		
	</view>
</template>

<script>
	import uniList from '../../components/uni-list/uni-list.vue'
	import uniListItem from '../../components/uni-list-item/uni-list-item.vue'
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
