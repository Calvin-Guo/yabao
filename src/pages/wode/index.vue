<template>
  <view class="page flex-col">
    
 
    <view class="section_1 flex-col">
      <view class="image-wrapper_2 flex-row justify-between">
        <image
          class="label_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_wode/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
		  @click="redirect()"
        />
        <image
          class="label_2"
          referrerpolicy="no-referrer"
          src="/static/lanhu_wode/SketchPng479a038380f4eaec622541f64c6b4fd5e927704841de40232f7026da7bdd8da3.png"
		  @click="redirect('/pages/shezhi/index')"
        />
      </view>
      <view class="box_1 flex-row">
        <view class="group_1 flex-col">
          <view class="image-wrapper_3 flex-col">
            <image
              class="label_3"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/SketchPng47b2e8272f832eedbc411d543ac4d392591cf9057e2a6a9beb9c41aea33172ad.png"
            />
          </view>
        </view>
        <view class="text-group_1 flex-col">
          <text class="text_1">漠河dancer</text>
          <text class="text_2">会员ID:2345980</text>
        </view>
        <view class="text-wrapper_1 flex-col">
          <text class="text_3">点击成为会员</text>
        </view>
      </view>
     
    </view>
    <view class="section_2 flex-col">
      <view class="group_2 flex-col"></view>
      <view class="group_3 flex-row" @click="redirect('/pages/bizhi/index')">
        <text class="text_5">每日壁纸</text>
        <text class="text_6">获取每日最新壁纸</text>
        <image
          class="label_5"
          referrerpolicy="no-referrer"
          src="/static/lanhu_wode/c42da245e6374631a6b0da033c2565bd_mergeImage.png"
        />
      </view>
      <view class="group_4 flex-col">
        <view class="group_5 flex-row justify-between">
          <view class="image-text_1 flex-row justify-between">
            <image
              class="label_6"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/SketchPng29aa1d36cd24d4e87d3d8657eaccf60a0acf091af0695332af9b7e3c97bb3bd3.png"
            />
            <text class="text-group_2">联系客服鸭哥</text>
          </view>
          <view class="image-text_2 flex-row justify-between">
            <text class="text-group_3">人工客服</text>
            <image
              class="label_7"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/48406717183e4232925fa92ae82ea734_mergeImage.png"
            />
          </view>
        </view>
        <view class="group_6 flex-row justify-between"@click="()=>{$refs.guanzhu.open();}">
          <view class="image-text_3 flex-row justify-between" >
            <view class="image-wrapper_5 flex-col">
              <image
                class="label_8"
                referrerpolicy="no-referrer"
                src="/static/lanhu_wode/SketchPngb9cec90a38f0a730c5310f1098e4885f7351da1f54a3bab8051baf8783d40acf.png"
              />
            </view>
            <text class="text-group_4">关注我们</text>
          </view>
          <view class="image-text_4 flex-row justify-between">
            <text class="text-group_5">
              鸭宝查询&nbsp;&nbsp;手机验机鉴定专家
            </text>
            <image
              class="label_9"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/24063333f3844d4aab2c90ed61f2a4d0_mergeImage.png"
            />
          </view>
        </view>
        <view class="group_7 flex-row justify-between">
          <view class="image-text_5 flex-row justify-between">
            <image
              class="label_10"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/6989b49829f040d0978a1b013117f688_mergeImage.png"
            />
            <text class="text-group_6">关于鸭宝查询</text>
          </view>
          <view class="image-text_6 flex-row justify-between">
            <text class="text-group_7">隐私政策</text>
            <image
              class="label_11"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/dc7799c8fdc14edd9c89d6544edf28e7_mergeImage.png"
            />
          </view>
        </view>
      </view>
      <view class="text-wrapper_2 flex-col">
        <text class="text_7">退出</text>
      </view>
      <text class="text_8">注销账户</text>
      <view class="group_8 flex-col">
        <view class="group_9 flex-row justify-end">
          <text class="text_9">0.00</text>
          <text class="text_10">个</text>
          <text class="text_11">余额迁徙</text>
          <view class="text-wrapper_3 flex-col" @click='()=>{$refs.chongzhi.open()}'>
            <text class="text_12">充值</text>
          </view>
          <view class="box_3 flex-col"></view>
          <text class="text_13">Y币金额：</text>
        </view>
        <image
          class="image_4"
          referrerpolicy="no-referrer"
          src="/static/lanhu_wode/SketchPngf827c35e461dcd912d68364e5d5cd2938fa06b572b424e469cca9420be9e6673.png"
        />
        <view class="group_10 flex-row" >
          <view class="image-text_7 flex-row justify-between" @click="redirect('/pages/xiaofeijilu/index')">
            <image
              class="label_12"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/9fcd1138266e49f6a420ae1594161aaa_mergeImage.png"
            />
            <text class="text-group_8">消费/充值记录</text>
          </view>
          <image
            class="image_5"
            referrerpolicy="no-referrer"
            src="/static/lanhu_wode/SketchPng44ebe16656c597fdcd2e0a131f56c4b190eed1e8dc10cf357173e3da0740be30.png"
          />
          <view class="image-text_8 flex-row justify-between" @click="redirect('/pages/chaxunjilu/index')">
            <image
              class="label_13"
              referrerpolicy="no-referrer"
              src="/static/lanhu_wode/cc788a12d23d4cb3b68d73ff957784f4_mergeImage.png"
            />
            <text class="text-group_9">历史查询记录</text>
          </view>
        </view>
      </view>
      
    </view>
	<Chongzhi ref='chongzhi'/>
	<uni-popup ref="guanzhu" type="dialog">
		<image
		  src="/static/guanzhu.png"
		  style="width: 344px;height:393px"
		/>
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
      constants: {}
    };
  },
  methods: {
	  redirect:(url)=>{
		  if(url){
			  uni.navigateTo({
				url:url,
				animationType:"pop-in"
			  })
		  }else{
			  uni.navigateBack({
			  	
			  })
		  }
		  
	  }
  }
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.response.css';
</style>
