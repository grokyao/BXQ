<template>
    <view>
		<uni-list>
		    <uni-list-item title="牛魔王,男,58岁" 
				note="就诊日期:2019-1-22"
				showBadge="true" 
		        show-extra-icon="true" 
		        :extra-icon="{color: '#FD962E',size: '60',type: 'contact'}"
				v-on:click="gotoHuanzhexinxi()">
		    </uni-list-item>
		</uni-list>	
        <view class='feedback-title'>
            <text>中医诊断</text>

        </view>

        <view class="feedback-body">
			<view style="text-align: center;" >中医证型</view>
					<bjx-inputs ref='inputs1' placeholder='证型' @list="getDataZhengxing" @select='select1' @focus="focus1" @blur="blur1"/>
			
			<view class="uni-form-item uni-column">
				<view class="title">中医病名</view>
				<input class="uni-input" focus placeholder="证型" />
			</view>
			<view class="uni-form-item uni-column">
				<view class="title">中医证型</view>
				<input class="uni-input" focus placeholder="证型" />
			</view>

			<view class="uni-form-item uni-column">
				<view class="title">中医病名</view>
				<input class="uni-input" focus placeholder="证型" />
			</view>
            </view>
 
        <button type="default" class="feedback-submit" @tap="send">保存</button>
		
    </view>
</template>

<script>
    import uniList from '.../../../components/uni-list/uni-list.vue'
    import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
    import uniTag from "../../../components/uni-tag/uni-tag.vue" //标签组件
	import BjxInputs from '../../../components/bjx-inputs/bjx-inputs.vue'//远程搜索输入
	export default {
        data() {
            return {
                stars: [1, 2, 3, 4, 5],
                imageList: [],
                sendDate: {
                    score: 0,
                    content: "",
                    contact: ""
                },
				dataZhengxing: [
					{id: 1, value: '胃热滞脾'},
					{id: 2, value: '脾虚不运'},
					{id: 3, value: '脾肾阳虚'},
					{id: 4, value: '痰湿淤阻'},
					{id: 5, value: '气滞血瘀'}
				],
				dataZhongyibingming: [
					{id: 1, value: '肥胖病'},
					{id: 2, value: '伤筋病'},
					{id: 3, value: '眩晕病'},
					{id: 4, value: '不孕病'},
					{id: 5, value: '痰饮病'}
				]
            }
        },
        onLoad() {
            
        },
        methods: {
            close(e){
                this.imageList.splice(e,1);
            },
            //页面跳转
            gotoHuanzhexinxi(){
            	uni.navigateTo({
            	url: '../../room/huanzhexinxi/huanzhexinxi'
            	});
            },
			// 远程加载数据 返回一个对象，{value: 输入框值, callback: 回调函数}
			getDataZhengxing(e) {
				console.log(e)
				if(!e.value){
					e.callback(this.dataZhengxing)
				}else{
					let data = []
					this.dataZhengxing.forEach(item=>{
						if(item.indexOf(e.value) > -1){
							data.push(item)
						}
					})
					e.callback(data)
				}
			},
			getData2(e) {
				console.log(e)
				this.value = e.value
				if(!e.value){
					e.callback(this.data2)
				}else{
					let data = []
					this.data2.forEach(item=>{
						if(item.value.indexOf(e.value) > -1){
							data.push(item)
						}
					})
					e.callback(data)
				}
			},
			select1(value){
				console.log(1,value)
			},
			select2(value){
				this.value = value.value
				console.log(2,value)
			},
			// 若要在父组件动态改变bjx-inputs组件中的值 请直接调用组件中的setValue方法
			setInputsValue(){
				this.$refs.inputs1.setValue(this.value)
			},
			focus1(e){
				console.log('框1聚焦', e)
			},
			blur1(e){
				console.log('框1失焦', e)
			}
        },
		components: {
			uniList,uniListItem,uniTag,BjxInputs
		}
    }
</script>

<style>

    page {
        background-color: #EFEFF4;
    }
    view{
        font-size: 28upx;
    }
    .input-view {
        font-size: 28upx;
    }
    .close-view{
        text-align: center;line-height:14px;height: 16px;width: 16px;border-radius: 50%;background: #FF5053;color: #FFFFFF;position: absolute;top: -6px;right: -4px;font-size: 12px;
    }
    /* 上传 */
    
    .uni-tag {
    	margin: 20upx;
    }
    
    /*文本输入*/
	.feedback-title {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		padding: 20upx;
		color: #333333;
		font-size: 40upx;
	}
    .feedback-textare {
    	height: 200upx;
    	font-size: 34upx;
    	line-height: 50upx;
    	width: 100%;
    	box-sizing: border-box;
    	padding: 20upx 30upx 0;
    }
    
</style>
