<template>
  <view class="page flex-col">
  
    <view class="box_2 flex-row">
      <image
        class="label_1"
        referrerpolicy="no-referrer"
        src="/static/lanhu_baogaoyemian/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
		@click="goBack"
      />
      <text class="text_1">验机报告</text>
      <text class="text_2" @click="goHome">返回首页</text>
    </view>
    <text class="text_3">
      备注文案：免费查询基础数据，精确鉴定请使用苹果GSX验机报告，支持苹果所有设备
    </text>
   
    
    <view class="box_5 flex-col">
      <view class="text-wrapper_1 flex-row justify-between">
        <text class="text_5">验机总分</text>
        <text class="text_6">36分</text>
      </view>
      <image
        class="image_3"
        referrerpolicy="no-referrer"
        src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
      />
      <view class="group_1 flex-row">
        <image
          class="image_4"
          referrerpolicy="no-referrer"
          src="/static/lanhu_baogaoyemian/SketchPngbdc24325818c353a2ea0e5b385f353a192aac3b838cfe054e264790bb614163a.png"
        />
        <view class="text-wrapper_2 flex-col">
          <text class="text_7">型号</text>
          <text class="text_8">容量</text>
          <text class="text_9">颜色</text>
        </view>
        <view class="group_2 flex-col">
          <view class="text-group_1 flex-col">
            <text class="text_10">MacBook&nbsp;Pro&nbsp;(13寸，M1，2020）</text>
            <text class="text_11">256GB</text>
          </view>
          <text class="text_12">原色钛金属</text>
        </view>
      </view>
      <view class="group_3 flex-row justify-between">
        <view class="box_6 flex-col">
          <text class="text_13">序列号</text>
          <text class="text_14">多行列表列表</text>
          <text class="text_15">短内容</text>
          <text class="text_16">超链</text>
          <text class="text_17">带跳转列表</text>
          <image
            class="image_5"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
          <image
            class="image_6"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
          <image
            class="image_7"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
          <image
            class="image_8"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
          <image
            class="image_9"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
          <image
            class="image_10"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
        </view>
        <view class="box_7 flex-col">
          <text class="text_18">DWDFKFDSFDSFDSLFJSDF</text>
          <view class="text-group_2 flex-col">
            <text class="text_19">
              列表文字模拟列表文字模拟列表文SGGGGDFDSGG列表文字模拟列表文字表文字模拟模拟列
            </text>
            <text class="text_20">短内容</text>
          </view>
          <text class="text_21">超链文字</text>
          <view class="box_8 flex-row justify-between">
            <text class="text_22">带按钮跳转文字</text>
            <view class="text-wrapper_3 flex-col">
              <text class="text_23">查看说明</text>
            </view>
          </view>
        </view>
      </view>
      <text class="text_24">以下是激活锁方面结果</text>
      <view class="group_4 flex-row justify-between">
        <view class="block_1 flex-col">
          <text class="text_25">高亮文字</text>
          <text class="text_26">高亮文字</text>
          <image
            class="image_11"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
          <image
            class="image_12"
            referrerpolicy="no-referrer"
            src="/static/lanhu_baogaoyemian/SketchPng6309d1e0eb1690db06ff821bc81a9b4c8fe2a5a5cdfb1622846393cc5c9359e6.png"
          />
        </view>
        <view class="text-wrapper_4 flex-col">
          <text class="text_27">高亮文字</text>
          <text class="text_28">高亮文字</text>
        </view>
      </view>
      <view class="text-wrapper_5 flex-col">
        <text class="text_29">图片占位</text>
      </view>
    </view>
  </view>
</template>
<script>
export default {
  data() {
    return {
      constants: {}
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
  }
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.response.css';
</style>
