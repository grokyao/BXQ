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
            <text>西医诊断</text>

        </view>

        <view class="feedback-body">
			<view class="uni-form-item uni-column">
				<view class="title">诊断</view>
				<input class="uni-input" focus placeholder="输入内容" />
			</view>

			<view class="uni-form-item uni-column">
				<view class="title">阶段</view>
				<input class="uni-input" focus placeholder="输入内容" />
			</view>
			
            </view>
 
        <button type="default" class="feedback-submit" @tap="send">保存</button>
		
    </view>
</template>

<script>
    import uniList from '.../../../components/uni-list/uni-list.vue'
    import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
    import uniTag from "../../../components/uni-tag/uni-tag.vue" //标签组件
	export default {
        data() {
            return {
                stars: [1, 2, 3, 4, 5],
                imageList: [],
                sendDate: {
                    score: 0,
                    content: "",
                    contact: ""
                }
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
        },
		components: {
			uniList,uniListItem,uniTag
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
