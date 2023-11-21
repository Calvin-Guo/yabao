<template>
  <view class="page flex-col">
    
    <view class="box_2 flex-col">
      <view class="group_1 flex-col">
        <view class="group_2 flex-row justify-between">
          <image
            class="label_2"
            referrerpolicy="no-referrer"
            src="/static/lanhu_xiaofeijilu/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
			@click="goBack"
          />
          <text class="text_2" @click="goHome">返回首页</text>
        </view>
        <view class="group_3 flex-row">
          <text class="text_3" :style="{fontWeight: activeLeft?'600':'500'}" @click="activeLeft=true">消费记录（近1年）</text>
          <image
            class="image_2"
            referrerpolicy="no-referrer"
            src="/static/lanhu_xiaofeijilu/SketchPng63accdbfeeccd6737065aa343d8f847f6a327604d9bf889f7163e40ea45c194b.png"
          />
          <text class="text_4" :style="{fontWeight: !activeLeft?'600':'500'}" @click="activeLeft=false">充值记录</text>
        </view>
        <view class="group_4 flex-row" :style="{marginLeft: activeLeft?'15.46vw':'66vw'}">
          <view class="box_3 flex-col"></view>
        </view>
      </view>
     <view class="xfjl flex-col" :style="{right:activeLeft?'0':'100vw'}">
		  <view class="list_1 flex-col">
			<view
			  class="list-items_1 flex-row"
			  v-for="(item, index) in loopData0"
			  :key="index"
			>
			  <view class="text-group_2 flex-col">
				<text class="text_9" v-html="item.lanhutext0"></text>
				<text class="text_10" v-html="item.lanhutext1"></text>
			  </view>
			  <image
				class="image_4"
				referrerpolicy="no-referrer"
				:src="item.lanhuimage0"
			  />
			  <text class="text_11" v-html="item.lanhutext2"></text>
			  <text class="text_12" v-html="item.lanhutext3"></text>
			</view>
		  </view>
		  <view class="group_6 flex-row">
			<view class="group_7 flex-col"></view>
			<text class="text_13">没有更多了</text>
			<view class="group_8 flex-col"></view>
		  </view>
	  </view>
	  <view class="czjl flex-col" :style="{left:activeLeft?'100vw':'0'}">
	  	<view class="group_9 flex-col">
	  	  <view class="list_2 flex-col">
	  	    <view
	  	      class="list-items_2 flex-col"
	  	      v-for="(item, index) in loopData1"
	  	      :key="index"
	  	    >
	  	      <view class="text-wrapper_1 flex-row">
	  	        <text class="text_5" v-html="item.lanhutext0"></text>
	  	        <text class="text_6" v-html="item.lanhutext1"></text>
	  	        <text class="text_7" v-html="item.lanhutext2"></text>
	  	        <text class="text_8" v-html="item.lanhutext3"></text>
	  	      </view>
	  	      <image
	  	        class="image_3"
	  	        referrerpolicy="no-referrer"
	  	        :src="item.lanhuimage0"
	  	      />
	  	    </view>
	  	  </view>
		 
	  	</view>
		<view class="group_6 flex-row">
					<view class="group_7 flex-col"></view>
					<text class="text_13">没有更多了</text>
					<view class="group_8 flex-col"></view>
		</view>
	  </view>
    </view>
    
  </view>
</template>
<script>
export default {
  data() {
    return {
		activeLeft:true,
      loopData0: [
        {
          lanhutext0: '苹果SX验机报告（pro）报告',
          lanhutext1: '2023-10-25&nbsp;17:50:23',
          lanhuimage0:
            'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPng5439e44723eef50d6206ec2a37321ba7e6351b0beb87d0c8b7690777fc38e199',
          lanhutext2: '-50',
          lanhutext3: '币'
        },
        {
          lanhutext0: '苹果SX验机报告（pro）报告',
          lanhutext1: '2023-10-25&nbsp;17:50:23',
          lanhuimage0:
            'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPng5439e44723eef50d6206ec2a37321ba7e6351b0beb87d0c8b7690777fc38e199',
          lanhutext2: '-50',
          lanhutext3: '币'
        },
        {
          lanhutext0: '苹果SX验机报告（pro）报告',
          lanhutext1: '2023-10-25&nbsp;17:50:23',
          lanhuimage0:
            'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPng5439e44723eef50d6206ec2a37321ba7e6351b0beb87d0c8b7690777fc38e199',
          lanhutext2: '-50',
          lanhutext3: '币'
        }
      ],
	  loopData1: [
	    {
	      lanhutext0: '2023-10-25&nbsp;17:50:23',
	      lanhutext1: '充值',
	      lanhutext2: '50',
	      lanhutext3: '元',
	      lanhuimage0:
	        'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPngf6f52a9231bfa293a7c62624bb4b335ede9734f9f189d75ecbba6c4386061039'
	    },
	    {
	      lanhutext0: '2023-10-25&nbsp;17:50:23',
	      lanhutext1: '充值',
	      lanhutext2: '50',
	      lanhutext3: '元',
	      lanhuimage0:
	        'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPngf6f52a9231bfa293a7c62624bb4b335ede9734f9f189d75ecbba6c4386061039'
	    },
	    {
	      lanhutext0: '2023-10-25&nbsp;17:50:23',
	      lanhutext1: '充值',
	      lanhutext2: '50',
	      lanhutext3: '元',
	      lanhuimage0:
	        'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPngf6f52a9231bfa293a7c62624bb4b335ede9734f9f189d75ecbba6c4386061039'
	    },
	    {
	      lanhutext0: '2023-10-25&nbsp;17:50:23',
	      lanhutext1: '充值',
	      lanhutext2: '50',
	      lanhutext3: '元',
	      lanhuimage0:
	        'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPngf6f52a9231bfa293a7c62624bb4b335ede9734f9f189d75ecbba6c4386061039'
	    },
	    {
	      lanhutext0: '2023-10-25&nbsp;17:50:23',
	      lanhutext1: '充值',
	      lanhutext2: '50',
	      lanhutext3: '元',
	      lanhuimage0:
	        'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPngf6f52a9231bfa293a7c62624bb4b335ede9734f9f189d75ecbba6c4386061039'
	    }
	  ],
      constants: {}
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
  },
	  
  mounted(){
	  uni.showTabBar();
  }
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.response.css';
</style>
