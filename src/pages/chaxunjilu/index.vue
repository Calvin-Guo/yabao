<template>
  <view class="page flex-col">
   
    <view class="box_2 flex-col">
      <view class="group_1 flex-row">
        <image
          class="label_2"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chaxunjilu/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
		  @click="goBack"
        />
        <text class="text_2">历史查询记录</text>
        <text class="text_3" @click="showDrawer()">搜索记录</text>
      </view>
      <view class="group_2 flex-row">
        <view class="image-text_1 flex-row justify-between">
          <image
            class="label_3"
            referrerpolicy="no-referrer"
            src="/static/lanhu_chaxunjilu/SketchPngcc0e3440fdaae0210541fb45377f48e10219d4f5af13e162dd276e6151efedcc.png"
          />
          <text class="text-group_1">在记录上向左滑动可删除记录</text>
        </view>
      </view>
      <view class="list_1 flex-col">
        <view
          class="list-items_1 flex-row justify-end"
          v-for="(item, index) in loopData0"
          :key="index"
		  
		  @touchstart="drawStart" @touchmove="drawMove(index,$event)" @touchend="drawEnd(index,$event)" @click="addX(index)"
        >
          <view class="text-wrapper_1 flex-col">
            <text class="text_4" v-html="item.lanhutext0"></text>
          </view>
          <view class="text-group_2 flex-col">
            <text class="text_5" v-html="item.lanhutext1"></text>
            <text class="text_6" v-html="item.lanhutext2"></text>
            <text class="text_7" v-html="item.lanhutext3"></text>
          </view>
          
		  <view
		    class="image-wrapper_2 flex-col"
			style="background: rgba(0,0,0,1)"
		  >
			  <image
				class="thumbnail_1"
				referrerpolicy="no-referrer"
				src="/static/lanhu_chaxunjilu/SketchPngd0e1741e1c6125c6b07250d7cc505dd87bcd77a0085038f71e33405571be5512.png"
			  /> 
		  </view>
		  <view
		    class="image-wrapper_2 flex-col delete"
		    style="background: rgba(255,98,98,1)"
			:style="{right:item.showDel?'0':'-10vw'}"
			ref="box_center"
		  >
		    <image
		      class="label_4"
		      referrerpolicy="no-referrer"
		      src="/static/lanhu_chaxunjilu/SketchPng3fb3339a8ca824b6d1503669c8f00fe7ef9d3af16e1e1ae31f926f818c02d181.png"
		    />
		    
		  </view>
        </view>
      </view>
     
      <view class="group_5 flex-row">
        <view class="block_1 flex-col"></view>
        <text class="text_12">没有更多了</text>
        <view class="block_2 flex-col"></view>
      </view>
    </view>
    <uni-drawer ref="showRight" mode="right" :mask-click="false" >
    			<scroll-view style="height: 100%;" scroll-y="true">
    				<view class="group_6 flex-row" >
    				 
    				  <text class="text_13">请选择检索条件</text>
    				  <text class="text_14" @click="closeDrawer()">×</text>
    				</view>
    				<view class="drawer_content">
						<div class="drawer_notice">请选择查询类型</div>
						<zxz-uni-data-select v-model="searchType" filterable :localdata="selectList" @inputChange="inputChange"
							@change="change"></zxz-uni-data-select>
						<div class="drawer_notice">请输入查询IMEI/SN</div>
						<input class="drawer_input"  placeholder="请输入查询IMEI/SN" />
						<div class="drawer_notice">请选择查询时间</div>
						<uni-datetime-picker v-model="range" :border='false' type="daterange" @maskClick="maskClick" class="dateTimePicker" />
					<view class="flex-row justify-between">
						<div class="submit">提交</div>
						<div class="cancel">重置</div>
					</view>
					</view>
					
    			</scroll-view>
				
    		</uni-drawer>
  </view>
</template>
<script>
export default {
  data() {
    return {
		clientX:0,
      loopData0: [
        {
          lanhutext0: '图片配图',
          lanhutext1: '查询内容的标题',
          lanhutext2: 'C02G67CAQ05F',
          lanhutext3: '2022-02-15&nbsp;13:57:54',
          lanhuBg3: 'rgba(0,0,0,1.000000)',
          slot1: 1
        },
        {
          lanhutext0: '图片配图',
          lanhutext1: '查询内容的标题',
          lanhutext2: 'C02G67CAQ05F',
          lanhutext3: '2022-02-15&nbsp;13:57:54',
          lanhuBg3: 'rgba(255,98,98,1.000000)',
          slot2: 2
        }
      ],
      constants: {},
	  selectList:[],
	  searchType:'',
	  range:[]
	  
    };
  },
  methods: {
	  goBack:()=>{
	  		  uni.switchTab({
	  		  	url:'/pages/wode/index'
	  		  })
	  },
	  search:()=>{
	  		 this.showDrawer()
	  },
	  showDrawer() {
	  				this.$refs.showRight.open();
	  			},
	  			closeDrawer() {
	  				this.$refs.showRight.close();
	  			},
	  // 开始触摸
	  			drawStart(e) {
	  				this.clientX = e.changedTouches[0].clientX
	  			},
	  			// 触摸过程
	  			drawMove(id, e) {
	  				var endX = e.changedTouches[0].clientX;
	  				let diff = endX - this.clientX;
	  				if (Math.abs(diff) <= 130 && diff < 0) {
	  					let box_center = this.$refs.box_center[id]
	  					box_center.$el.style.right = diff + 'px'
	  				}
	  
	  			},
	  			// 结束触摸
	  			drawEnd(id, e) {
	  				// console.log('结束',e.changedTouches[0]);
	  				var endX = e.changedTouches[0].clientX;
	  				let diff = endX - this.clientX;
	  				let box_center = this.$refs.box_center[id]
	  				if (Math.abs(diff) > 20) {
	  					// console.log('移动',diff,id,e);
	  					if (diff > 0) {
	  						box_center.$el.style.right = '-10vw'
	  					} else {
	  						box_center.$el.style.right = '0'
	  					}
	  
	  				}else{
	  					box_center.$el.style.right = '0'
	  				}
	  
	  			},
	  			// 点击恢复原始数据
	  			addX(id) {
	  				let box_center = this.$refs.box_center[id]
	  				box_center.$el.style.right = '-10vw'
	  			},
					
				inputChange(){
				},
				change(){
					
				}
	
  }
};
</script>
<style lang='css' scoped>
@import '../common/common.css';
@import './assets/style/index.response.css';
</style>
