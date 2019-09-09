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
        <view class='feedback-title'>
            <text>主诉</text>
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
        <uni-tag text="乏力" type="default" :circle="true"></uni-tag>
        <uni-tag text="头痛" type="warning" :circle="true"></uni-tag>
        <uni-tag text="伴" type="default" :circle="true"></uni-tag>
        <uni-tag text="失眠" type="warning" :circle="true"></uni-tag>
        <uni-tag text="汗多" type="default" :circle="true"></uni-tag>
        <uni-tag text="没胃口" type="warning" :circle="true"></uni-tag>
        <uni-tag text="1天" type="default" :circle="true"></uni-tag>
        <uni-tag text="2天" type="warning" :circle="true"></uni-tag>
        <uni-tag text="一周" type="default" :circle="true"></uni-tag>
        <uni-tag text="二周" type="warning" :circle="true"></uni-tag>
        <uni-tag text="三周" type="default" :circle="true"></uni-tag>
        <uni-tag text="一个月" type="warning" :circle="true"></uni-tag>
        <uni-tag text="二个月" type="default" :circle="true"></uni-tag>
        <uni-tag text="半年" type="warning" :circle="true"></uni-tag>
        <uni-tag text="一年" type="default" :circle="true"></uni-tag>
        <uni-tag text="两年" type="warning" :circle="true"></uni-tag>
        <uni-tag text="余" type="default" :circle="true"></uni-tag>
    </view>
</template>

<script>
    import uniList from '.../../../components/uni-list/uni-list.vue'
    import uniListItem from '../../../components/uni-list-item/uni-list-item.vue'
    import uniTag from "../../../components/uni-tag/uni-tag.vue" //标签组件
	export default {
        data() {
            return {
                msgContents: ["头晕伴耳鸣2周余", "体胖伴乏力半年余", "失眠三年", "胃胀伴无食欲月余"],
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
            
        },
		components: {
			uniList,uniListItem,uniTag
		}
    }
</script>

<style>
    @font-face {
    	font-family: uniicons;
    	font-weight: normal;
    	font-style: normal;
    	src: url('https://img-cdn-qiniu.dcloud.net.cn/fonts/uni.ttf') format('truetype');
    }
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
    .uni-uploader {
    	flex: 1;
    	flex-direction: column;
    }
    .uni-uploader-head {
    	display: flex;
    	flex-direction: row;
    	justify-content: space-between;
    }
    .uni-uploader-info {
    	color: #B2B2B2;
    }
    .uni-uploader-body {
    	margin-top: 16upx;
    }
    .uni-uploader__files {
    	display: flex;
    	flex-direction: row;
    	flex-wrap: wrap;
    }
    .uni-tag {
    	margin: 20upx;

    }
    .uni-uploader__img {
    	display: block;
    	width: 210upx;
    	height: 210upx;
    }
    .uni-uploader__input-box {
    	position: relative;
    	margin:10upx;
    	width: 208upx;
    	height: 208upx;
    	border: 2upx solid #D9D9D9;
    }
    .uni-uploader__input-box:before,
    .uni-uploader__input-box:after {
    	content: " ";
    	position: absolute;
    	top: 50%;
    	left: 50%;
    	-webkit-transform: translate(-50%, -50%);
    	transform: translate(-50%, -50%);
    	background-color: #D9D9D9;
    }
    .uni-uploader__input-box:before {
    	width: 4upx;
    	height: 79upx;
    }
    .uni-uploader__input-box:after {
    	width: 79upx;
    	height: 4upx;
    }
    .uni-uploader__input-box:active {
    	border-color: #999999;
    }
    .uni-uploader__input-box:active:before,
    .uni-uploader__input-box:active:after {
    	background-color: #999999;
    }
    .uni-uploader__input {
    	position: absolute;
    	z-index: 1;
    	top: 0;
    	left: 0;
    	width: 100%;
    	height: 100%;
    	opacity: 0;
    }
    
    /*问题反馈*/
    .feedback-title {
    	display: flex;
    	flex-direction: row;
    	justify-content: space-between;
    	align-items: center;
    	padding: 20upx;
    	color: #8f8f94;
    	font-size: 40upx;
    }
    .feedback-star-view.feedback-title {
    	justify-content: flex-start;
    	margin: 0;
    }
    .feedback-quick {
    	position: relative;
    	padding-right: 40upx;
    }
    .feedback-quick:after {
    	font-family: uniicons;
    	font-size: 40upx;
    	content: '\e581';
    	position: absolute;
    	right: 0;
    	top: 50%;
    	color: #bbb;
    	-webkit-transform: translateY(-50%);
    	transform: translateY(-50%);
    }
    .feedback-body {
    	background: #fff;
    }
    .feedback-textare {
    	height: 200upx;
    	font-size: 34upx;
    	line-height: 50upx;
    	width: 100%;
    	box-sizing: border-box;
    	padding: 20upx 30upx 0;
    }
    .feedback-input {
    	font-size: 34upx;
    	height: 50upx;
    	min-height: 50upx;
    	padding: 15upx 20upx;
    	line-height: 50upx;
    }
    .feedback-uploader {
    	padding: 22upx 20upx;
    }
    .feedback-star {
    	font-family: uniicons;
    	font-size: 40upx;
    	margin-left: 6upx;
    }
    .feedback-star-view {
    	margin-left: 20upx;
    }
    .feedback-star:after {
    	content: '\e408';
    }
    .feedback-star.active {
    	color: #FFB400;
    }
    .feedback-star.active:after {
    	content: '\e438';
    }
    .feedback-submit {
    	background: #007AFF;
    	color: #FFFFFF;
    	margin: 20upx;
    }
</style>
