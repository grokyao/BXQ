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
		<view class="uni-common-mt">
		    <view class="uni-form-item uni-column">
		            <view class="title">主诉</view>
		            <input class="uni-input" focus placeholder="输入内容,必填项" />
		    </view>
		</view>
		<button @click="openPopup">保存</button>
		
		<uni-tag text="快捷输入" type="warning" ></uni-tag>
		<uni-tag text="自定义快捷输入" type="success" :circle="true"></uni-tag>
		<uni-tag text="乏力" type="error" :circle="true"></uni-tag>
		<uni-tag text="头痛" type="warning" :circle="true"></uni-tag>
		<uni-tag text="伴" type="error" :circle="true"></uni-tag>
		<uni-tag text="失眠" type="warning" :circle="true"></uni-tag>
		<uni-tag text="汗多" type="error" :circle="true"></uni-tag>
		<uni-tag text="没胃口" type="warning" :circle="true"></uni-tag>
		<uni-tag text="1天" type="error" :circle="true"></uni-tag>
		<uni-tag text="2天" type="warning" :circle="true"></uni-tag>
		<uni-tag text="一周" type="error" :circle="true"></uni-tag>
		<uni-tag text="二周" type="warning" :circle="true"></uni-tag>
		<uni-tag text="三周" type="error" :circle="true"></uni-tag>
		<uni-tag text="一个月" type="warning" :circle="true"></uni-tag>
		<uni-tag text="二个月" type="error" :circle="true"></uni-tag>
		<uni-tag text="半年" type="warning" :circle="true"></uni-tag>
		<uni-tag text="一年" type="error" :circle="true"></uni-tag>
		<uni-tag text="两年" type="warning" :circle="true"></uni-tag>
		<uni-tag text="余" type="error" :circle="true"></uni-tag>
	</view>
	

</template>

<script>
	import uniList from '.../../../components/uni-list/uni-list.vue'
	import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
	import uniTag from "../../../components/uni-tag/uni-tag.vue" //标签组件
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
			}
		},
		components: {
			uniList,uniListItem,uniTag
		}
	}
</script>

<style>

</style>
