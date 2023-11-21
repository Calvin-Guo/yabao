<template>
  <view class="page flex-col">
 
    <view class="group_2 flex-col">
      <view class="box_1 flex-row justify-between">
        <image
          class="label_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chaxunx2fdancichaxun/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
		  @click="goBack"
        />
        <text class="text_1" @click="goHome">返回首页</text>
      </view>
      <view class="box_2 flex-row justify-between">
        <view class="group_3 flex-col"></view>
        <view class="text-group_1 flex-col">
          <text class="text_2">苹果基础查询</text>
          <text class="text_3">
            免费查询基础数据，精确鉴定请使用苹果GSX验机报告，支持苹果所有设备
          </text>
        </view>
      </view>
      <view class="box_3 flex-row">
		 
        <view v-if='!multiple' class="section_1 flex-row justify-between" @click="multiple=true">
          <text class="text_4">批量查询</text>
          <view class="text-wrapper_1 flex-col">
            <text class="text_5">NEW</text>
          </view>
        </view>
		<view v-if='multiple' class="block_5 flex-row">
		  <text class="text_35">批量查询</text>
		  <view class="text-wrapper_12 flex-col">
		    <text class="text_36">NEW</text>
		  </view>
		</view>
      </view>
	 <view v-if='multiple' class="text-wrapper_13 flex-col" @click="multiple=false">
	   <text class="text_42">单次查询</text>
	 </view>
    <view v-if='!multiple' class="text-wrapper_2 flex-col" >
       <text class="text_6">单次查询</text>
     </view>
    </view>
    <view class="text-wrapper_3 flex-col" :style="{marginTop:multiple?'117vw':'85vw'}">
      <text class="text_7">图片占位</text>
    </view>
   
    
    <view class="group_6 flex-col" :style="{paddingTop:multiple?'70vw':'38.73vw'}">
      <text class="text_9">温馨提示：</text>
      <view class="group_7 flex-row justify-between">
        <view class="text-wrapper_4 flex-col">
          <text class="text_10">1.</text>
          <text class="text_11">2.</text>
          <text class="text_12">3.</text>
        </view>
        <view class="text-wrapper_5">
          <text class="text_13">本查询为通过精确查询设备的</text>
          <text class="text_14">激活锁+网络锁+监管锁</text>
          <text class="paragraph_1">
            ，不支持Mac查询
            <br />
            所有查询数据均确保精确，支持未激活的设备查询
          </text>
          <text class="paragraph_2">
            <br />
            价格：
          </text>
          <text class="text_15">6</text>
          <text class="text_16">Y币/次（约人民币2.4元至6.0元）</text>
          <text class="text_17"></text>
        </view>
      </view>
      <view class="text-wrapper_6">
        <text class="text_18">以下是</text>
        <text class="text_19">示例结果</text>
        <text class="text_20">仅供查询前预览</text>
      </view>
      <view class="group_8 flex-col" :style="{height:multiple?'82vw':'49.47vw'}">
        <view class="text-wrapper_7 flex-col">
          <input v-if='!multiple' class="text_21" placeholder="请输入序列号"></input>
		  <textarea v-else class="text_21" placeholder="多个序列号/IMEI请以换行隔开"></textarea>
        </view>
        <text class="text_22">*如存在多个IMEI,请输入IMEI1</text>
        <view class="box_4 flex-row justify-between">
          <view class="text-wrapper_8 flex-col">
            <text class="text_23">AI识别</text>
          </view>
          <view class="text-wrapper_9 flex-col" @click='confirm'>
            <text class="text_24">查询</text>
          </view>
        </view>
        <text class="text_25">
          设置&nbsp;&gt;&nbsp;通用&nbsp;&gt;&nbsp;关于本机&nbsp;&gt;&nbsp;序列号，长按复制即可
        </text>
      </view>
      <view class="text-wrapper_10 flex-col" :style="{top:multiple?'97.5vw':'66.4vw'}" @click='()=>{$refs.chongzhi.open()}'>
        <text class="text_26">点击充值</text>
      </view>
    </view>
	<Chongzhi ref='chongzhi'/>
	<uni-popup ref="submitPop" type="dialog">
		<uni-popup-dialog mode="base" title='确认'  content="总余额48个Y币，本次将扣除1个 请确认您的序列号/IMEI：rwerwererwerew是否正确，错误将不予退款哦！" @close="close" @confirm="submit">
		</uni-popup-dialog>
	</uni-popup>
  </view>
</template>
<script>
	import Chongzhi from "@/pages/chongzhi/index"
export default {
	components:{
		Chongzhi:Chongzhi
	},
  data() {
    return {
      multiple:false
    };
  },
  methods: {
	  goBack(){
	  		  uni.navigateBack({
	  		  	
	  		  })
	  },
	  goHome(){
	  		  uni.switchTab({
	  		  	url:"/pages/shouye/index"
	  		  })
	  },
	  confirm(value){
		
		this.$refs.submitPop.open();
	  },
	  submit(){
		  uni.navigateTo({
		  	url:"/pages/baogaoyemian/index"
		  })
	  },
	  close(){
		  this.$refs.submitPop.close()
	  }
  }
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.response.css';
</style>
