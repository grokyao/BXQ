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
            <text>问诊</text>
			<view class="">
				<text class="feedback-quick" @tap="chooseMsg">快速键入</text>
			</view>  
        </view>

        <view class="feedback-body">
			
            <textarea placeholder="输入内容,必填项..." v-model="sendDate.content" class="feedback-textare" />
            </view>
 
        <button type="default" class="feedback-submit" @tap="send">保存</button>
		

		
        <uni-tag text="快捷输入" type="warning" ></uni-tag>
        <uni-tag text="自定义快捷输入" type="success" :circle="true"></uni-tag>
        <uni-tag text="头痛" type="default" :circle="true"></uni-tag>
        <uni-tag text="头晕" type="warning" :circle="true"></uni-tag>
        <uni-tag text="耳鸣" type="default" :circle="true"></uni-tag>
        <uni-tag text="口苦" type="warning" :circle="true"></uni-tag>
        <uni-tag text="口干" type="default" :circle="true"></uni-tag>
        <uni-tag text="乳房胀痛" type="warning" :circle="true"></uni-tag>
        <uni-tag text="心悸" type="default" :circle="true"></uni-tag>
        <uni-tag text="胸闷" type="warning" :circle="true"></uni-tag>
        <uni-tag text="打嗝" type="default" :circle="true"></uni-tag>
        <uni-tag text="胃胀" type="warning" :circle="true"></uni-tag>
        <uni-tag text="反酸" type="default" :circle="true"></uni-tag>
        <uni-tag text="腹胀" type="warning" :circle="true"></uni-tag>
        <uni-tag text="失眠" type="default" :circle="true"></uni-tag>
        <uni-tag text="多梦" type="warning" :circle="true"></uni-tag>
        <uni-tag text="痛经" type="warning" :circle="true"></uni-tag>
		<uni-tag text="月经先期" type="warning" :circle="true"></uni-tag>
		<uni-tag text="月经后期" type="warning" :circle="true"></uni-tag>
		<uni-tag text="月经不定期" type="warning" :circle="true"></uni-tag>
		<uni-tag text="闭经" type="warning" :circle="true"></uni-tag>
    </view>
</template>

<script>
    import uniList from '.../../../components/uni-list/uni-list.vue'
    import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
    import uniTag from "../../../components/uni-tag/uni-tag.vue" //标签组件
	export default {
        data() {
            return {
                msgContents: ["头晕头痛", "胃胀，反酸", "失眠有噩梦", "痛经有血块"],
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
            chooseMsg() { //快速输入
                uni.showActionSheet({
                    itemList: this.msgContents,
                    success: (res) => {
                        this.sendDate.content = this.msgContents[res.tapIndex];
                    }
                })
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
