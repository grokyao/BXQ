<template>
	<view>
		
	<uni-list>
	    <uni-list-item title="患者" 
			note="待诊49人,已诊1788人"
			showBadge="true" badgeText="8"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="医案" 
			note="医案18个,已读120人"
			showBadge="true" badgeText="2"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'info-filled'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="会诊" 
			note="会诊5个,结束126个"
			showBadge="true" badgeText="5"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'navigate'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="考试" 
			note="已报考试,距考试60天"
			showBadge="true" badgeText="1"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'gear'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="课程" 
			note="在线课程3个,线下课程2个"
			showBadge="true" badgeText="5"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'list'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="论坛" 
			note="新话题7个,总话题12003个"
			showBadge="true" badgeText="7"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'chatboxes'}">
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
