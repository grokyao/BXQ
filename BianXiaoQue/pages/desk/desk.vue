<template>
	<view>
	<uni-list>
	    <uni-list-item title="牛魔王,男,58岁" 
			note="就诊日期:2019-1-22"
			showBadge="true" 
	        show-extra-icon="true" 
	        :extra-icon="{color: '#FD962E',size: '60',type: 'contact'}">
	    </uni-list-item>
	</uni-list>	
		
	<uni-collapse @change="change">
	    <uni-collapse-item title="病历">
	        <uni-list>
            <uni-list-item 	title="主诉" 
							note="主诉内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}"
							v-on:click="gotoIndex()">
			</uni-list-item>
			<uni-list-item 	title="现病史"
							note="现病史内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="望诊"
							note="望诊内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="闻诊"
							note="闻诊内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="问诊"
							note="闻诊内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="切诊"
							note="切诊内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>	
			<uni-list-item 	title="中医诊断"
							note="诊断内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="西医诊断"
							note="诊断内容,保存后显示"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>										
	        </uni-list>
		</uni-collapse-item>
	</uni-collapse>	
	
	<uni-collapse @change="change">
	    <uni-collapse-item title="检查检验">
	        <uni-list>
				<uni-list-item 	title="检验申请单" 
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
				</uni-list-item>
				<uni-list-item 	title="检查申请单"
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">		
				</uni-list-item>
			</uni-list>
		</uni-collapse-item>
	</uni-collapse>	
	
	<uni-collapse @change="change">
	    <uni-collapse-item title="中药处方">
	        <uni-list>
				<uni-list-item 	title="中药饮片处方" 
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
				</uni-list-item>
				<uni-list-item 	title="中药配方颗粒处方"
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">		
				</uni-list-item>
			</uni-list>
		</uni-collapse-item>
	</uni-collapse>	
	
	<uni-collapse @change="change">
	    <uni-collapse-item title="中成药/化学药处方">
	        <uni-list>
				<uni-list-item 	title="中成药处方" 
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}"
								>
				</uni-list-item>
				<uni-list-item 	title="化学药处方"
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">		
				</uni-list-item>
				<uni-list-item 	title="生物制剂处方"
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">		
				</uni-list-item>
			</uni-list>
		</uni-collapse-item>
	</uni-collapse>	
	
	<uni-collapse @change="change">
	    <uni-collapse-item title="处置单">
	        <uni-list>
				<uni-list-item 	title="处置单" 
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
				</uni-list-item>
			</uni-list>
		</uni-collapse-item>
	</uni-collapse>	
	
	<uni-collapse @change="change">
	    <uni-collapse-item title="其他项目">
	        <uni-list>
				<uni-list-item 	title="其他项目" 
								show-extra-icon="true" 
								:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
				</uni-list-item>
			</uni-list>
		</uni-collapse-item>
	</uni-collapse>	
	
	<uni-collapse @change="change">
	    <uni-collapse-item title="医嘱建议">
	        <uni-list>
	        <uni-list-item 	title="用药建议" 
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="作息建议"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="饮食建议"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="病情建议"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>
			<uni-list-item 	title="拒绝记录"
							show-extra-icon="true" 
							:extra-icon="{color: '#4cd964',size: '22',type: 'spinner'}">
			</uni-list-item>					
	        </uni-list>
		</uni-collapse-item>
	</uni-collapse>	
	
	<button @click="openPopup">完诊</button>
	    <uni-popup ref="popup" type="bottom">
	        <button>完诊</button>
			<button>暂存</button>
	        <button>转诊</button>
			<button>会诊</button>
			<button>作废</button>
	    </uni-popup>
		
	</view>
</template>

<script>
	import uniList from '../../components/uni-list/uni-list.vue'//列表组件
	import uniListItem from '../../components/uni-list-item/uni-list-item.vue'//列表组件
	import uniCollapse from'../../components/uni-collapse/uni-collapse.vue'// 折叠面板
	import uniCollapseItem from '../../components/uni-collapse-item/uni-collapse-item.vue'// 折叠面板
	import uniPopup from "../../components/uni-popup/uni-popup.vue"//弹出层组件
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
			//页面跳转
			gotoIndex(){
				uni.navigateTo({
				url: 'zhusu2/zhusu2'
				});
			},

			//弹出层组件
			openPopup(){
			            this.$refs.popup.open()
			},
			closePopup(){
			            this.$refs.popup.close()
			}
		},
		components: {
			uniList,uniListItem,  //列表组件
			uniCollapse,uniCollapseItem,  // 折叠面板
			uniPopup  //弹出层组件
		}

	}
</script>

<style>

</style>
