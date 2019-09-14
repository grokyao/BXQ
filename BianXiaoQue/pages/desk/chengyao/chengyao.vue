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
		<view class="uni-common-mt">
		    <view class="uni-form-item uni-column">
		            <view class="title">药品名称</view>
		            <input class="uni-input" focus placeholder="输入内容,必填项" />
		    </view>
		</view>
		<button @click="openPopup">保存</button>
		
	</view>
	

</template>

<script>
	import uniList from '.../../../components/uni-list/uni-list.vue'
	import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
	export default {
		data() {
			return {
				title: 'input',
				focus: false,
				inputValue: '',
				changeValue: ''
			}
		},
		methods: {
			onKeyInput: function(event) {
				this.inputValue = event.target.value
			},
			replaceInput: function(event) {
				var value = event.target.value;
				if (value === '11') {
					this.changeValue = '2';
				}
			},
			hideKeyboard: function(event) {
				if (event.target.value === '123') {
					uni.hideKeyboard();
				}
			},
			//页面跳转
			gotoIndex(){
				uni.navigateTo({
				url: '../../room/sufferer/sufferer'
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
