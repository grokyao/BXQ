<template>
	<view>
	<uni-list>
	    <uni-list-item title="大力诊所" 
			note="预约4人"
			showBadge="true" badgeText="4"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'home'}" 
			v-on:click="gotoIndex()">

	    </uni-list-item>
		
	</uni-list>

	<uni-list>
	    <uni-list-item title=" 华佗诊所" 
			note="预约15人"
			showBadge="true" badgeText="15"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'home'}">
	    </uni-list-item>
	</uni-list>

	<uni-list>
	    <uni-list-item title="天空诊所" 
			note="预约30人"
			showBadge="true" badgeText="30"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'home'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="海洋诊所" 
			note="预约0人"
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'home'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="待诊患者" 
	        show-extra-icon="true" 			
			showBadge="true" badgeText="4"
	        :extra-icon="{color: '#000000',size: '40',type: 'contact'}">
	    </uni-list-item>
	</uni-list>
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
	<uni-list>
	    <uni-list-item title="已诊患者"
	        show-extra-icon="true" 			
			showBadge="true" badgeText="2"
	        :extra-icon="{color: '#000000',size: '40',type: 'contact'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="王大锤" 
			note="风寒湿痹:伤筋病"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>	
	<uni-list>
	    <uni-list-item title="金角大王" 
			note="痰湿阻滞:肥胖症"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>			
	
	</view>
</template>

<script>
	import uniList from '../../components/uni-list/uni-list.vue'
	import uniListItem from '../../components/uni-list-item/uni-list-item.vue'
	import uniCollapse from'../../components/uni-collapse/uni-collapse.vue'
	import uniCollapseItem from '../../components/uni-collapse-item/uni-collapse-item.vue'
	//输出默认值
	export default {
		data() {
			return {
				
			}
		},
		//监听页面加载，其参数为上个页面传递的数据，参数类型为Object（用于页面传参）
		onLoad() {

		},
		methods: {
			gotoIndex(){
				uni.navigateTo({
				url: '../room/yysufferer/yysufferer'
				});
			},
		},
		components: {uniList,uniListItem,uniCollapse,uniCollapseItem}

	}
</script>

<style>

</style>
