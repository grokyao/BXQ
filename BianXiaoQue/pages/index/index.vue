<template>
	<view>
	<uni-list >
	    <uni-list-item title="患者" 
			:note="'待诊'+chengedate.daizhen+'人,'+'已诊'+chengedate.yizhen+'人'"
			showBadge="true" :badgeText="chengedate.benzhensuodaizhen"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'contact'}">
	    </uni-list-item>
	</uni-list>

	<uni-list>
	    <uni-list-item title="医案" 
			:note="'医案'+chengedate.yian+'个,'+'已读'+chengedate.yidu+'人'"
			showBadge="true" :badgeText="chengedate.yiangengxin"
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'info-filled'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="会诊" 
			:note="'会诊'+chengedate.xinhuizhen+'个,'+'结束'+chengedate.jieshuhuizhen+'人'"
			showBadge="true" :badgeText="chengedate.xinhuizhen"		
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'navigate'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="考试" 
			:note="'已报考试,距考试'+chengedate.kaoshi+'天'"
			showBadge="true" :badgeText="chengedate.fuxi"	
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'gear'}">
	    </uni-list-item>
	</uni-list>
	<uni-list>
	    <uni-list-item title="课程" 
			:note="'在线课程'+chengedate.zaixiankecheng+'个,'+'线下课程'+chengedate.xianxiakecheng+'人'"
			showBadge="true" :badgeText="chengedate.zongkecheng"		
	        show-extra-icon="true" 
	        :extra-icon="{color: '#000000',size: '32',type: 'list'}">
	    </uni-list-item>
	</uni-list>
	
	<uni-list>
	    <uni-list-item title="论坛" 
			:note="'新话题'+chengedate.xinhuati+'个,'+'总话题'+chengedate.zonghuati+'个'"
			showBadge="true" :badgeText="chengedate.zongkecheng"	
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
				//更新数据
				chengedate:{
					daizhen:"49",
					yizhen:"1788",
					benzhensuodaizhen:"8",
					yian:"18",
					yidu:"120",
					yiangengxin:"2",
					xinhuizhen:"10",
					jieshuhuizhen:"126",
					kaoshi:"60",
					fuxi:"3",
					zaixiankecheng:"3",
					xianxiakecheng:"2",
					zongkecheng:"5",
					xinhuati:"5",
					zonghuati:"12003"
				}
			}
		},
		onLoad() {
				//setInterval(function(){
				//	this.$set(this.changdata,'daizhen',++this.changdata.daizhen)	
				//},1000)
				//setInterval(function(){                   
				//接口获取数据
				//xxx=res.data                        
				//	this.$set(this.changdata,'daizhen',xxx)	
				//	},1000)
		},
		methods: {
		
		},
		components: {uniList,uniListItem}

	}
</script>

<style>

</style>
