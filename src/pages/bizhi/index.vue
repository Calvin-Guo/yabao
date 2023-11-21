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
		  <text style="margin-left: 16vw">每日壁纸</text>
          <text class="text_2" @click="goHome">返回首页</text>
        </view>
        <view class="group_3 flex-row">
          <text class="text_3" :style="{fontWeight: activeLeft?'600':'500'}" @click="activeLeft=true">PC壁纸（4K高清）</text>
          <image
            class="image_2"
            referrerpolicy="no-referrer"
            src="/static/lanhu_xiaofeijilu/SketchPng63accdbfeeccd6737065aa343d8f847f6a327604d9bf889f7163e40ea45c194b.png"
          />
          <text class="text_4" :style="{fontWeight: !activeLeft?'600':'500'}" @click="activeLeft=false">手机壁纸（1080P）</text>
        </view>
        <view class="group_4 flex-row" :style="{marginLeft: activeLeft?'15.46vw':'66vw'}">
          <view class="box_3 flex-col"></view>
        </view>
      </view>
     <view class="xfjl flex-col" :style="{right:activeLeft?'0':'100vw'}">
		  <view class="list_1 flex-col">
			<view
			  class="list-items_1"
			  v-for="(item, index) in loopData0"
			  :key="index"
			>
				<text>{{item.date}}</text>
				<image :src="item.url"></image>
			</view>
			<view class="group_6 flex-row">
						<view class="group_7 flex-col"></view>
						<text class="text_13">没有更多了</text>
						<view class="group_8 flex-col"></view>
			</view>
		  </view>
		 
	  </view>
	  <view class="czjl flex-col" :style="{left:activeLeft?'100vw':'0'}">
	  	<view class="group_9 flex-col">
	  	  <view class="list_2 flex-row">
	  	    <view
	  	      class="list-items_2"
	  	      v-for="(item, index) in loopData1"
	  	      :key="index"
	  	    >
	  	     <text>{{item.date}}</text>
	  	     <image :src="item.url"></image>
	  	    </view>
			<view class="group_6 flex-row">
				<view class="group_7 flex-col"></view>
				<text class="text_13">没有更多了</text>
				<view class="group_8 flex-col"></view>
			</view>
	  	  </view>
		 
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
          date: '2023-10-25',
          url:
            'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-21-pc.jpg?x-oss-process=image/resize,w_500,m_lfit',
        },
        {
          date: '2023-10-25',
          url:
            'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-21-pc.jpg?x-oss-process=image/resize,w_500,m_lfit',
        },
        {
          date: '2023-10-25',
          url:
            'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-21-pc.jpg?x-oss-process=image/resize,w_500,m_lfit',
        }
      ],
	  loopData1: [
	    {
	      date: '2023-10-25',
	      url:
	        'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-20-phone.jpg?x-oss-process=image/resize,w_300,m_lfit'
	    },
	    {
	      date: '2023-10-25',
	      url:
	        'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-20-phone.jpg?x-oss-process=image/resize,w_300,m_lfit'
	    },
	    {
	      date: '2023-10-25',
	      url:
	        'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-20-phone.jpg?x-oss-process=image/resize,w_300,m_lfit'
	    },
	    {
	      date: '2023-10-25',
	      url:
	        'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-20-phone.jpg?x-oss-process=image/resize,w_300,m_lfit'
	    },
	    {
	      date: '2023-10-25',
	      url:
	        'https://osm.oss-cn-shanghai.aliyuncs.com/wallPaper/2023-11-20-phone.jpg?x-oss-process=image/resize,w_300,m_lfit'
	    }
	  ],
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
