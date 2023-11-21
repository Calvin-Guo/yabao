<template>
  <view class="page flex-col">
   
    <view class="box_2 flex-col">
      <view class="group_1 flex-row ">
        <image
          class="label_2"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chaxunjilu/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
		  @click="goBack"
        />
        <text class="text_2">设置</text>
        <text class="text_3" @click="goHome">返回首页</text>
      </view>
     </view>
    <view class="box_3">
		<view v-for="(item,key) in config" :key="key" class="flex-row justify-between align-center">
			<view>{{item.name}}</view>
			<switch :checked='item.status' color="rgba(255, 229, 34, 1)" />
		</view>
	</view>
	<div class="button">保存</div>
  </view>
</template>
<script>
export default {
  data() {
    return {
      config:[
		  {
			  name:'生成报告关键信息加密',
			  status:true
		  },
		  {
			  name:'查询超过30秒自动推送报告',
			  status:true
		  }
	  ]
    };
  },
  methods: {
	  goBack:()=>{
	  		  uni.navigateBack({
	  		  	
	  		  })
	  },
	  goHome:()=>{
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
