<template>
  
	    <uni-popup ref="popup" type='dialog' :mask="true">
			<view class="block_1 flex-col">
			  <view class="group_1 flex-col">
			    <view class="section_1 flex-row">
			      <view class="text-wrapper_1">
			        <text class="text_1">当前选择实得</text>
			        <text class="text_2">{{gainCash}}</text>
			        <text class="text_3">Y币</text>
			        <text class="text_4">（1Y币≈{{coinNum}}元）</text>
			      </view>
			    </view>
			    <view class="section_2 flex-row">
			     <!-- <view v-if='activeCash==5' class="group_2 flex-col" @click="activeCash = 5">
			        <view class="text-wrapper_2 flex-row justify-between">
			          <text class="text_5">5</text>
			          <text class="text_6">元</text>
			        </view>
			        <view class="image-wrapper_1 flex-row">
			          <image
			            class="label_1"
			            referrerpolicy="no-referrer"
			            src="/static/lanhu_chongzhidanchuang/SketchPng3a4c5a3d6358825b758cd4f1c71149ab72ae599806e0f13d6b86dbd95bcb459f.png"
			          />
			        </view>
			      </view> -->
			      <view v-for="(item,key) in cashList" :key='key' class="group_3 flex-col justify-around" :class="item.num == activeCash?'activeCash':''" @click="activeCash = item.num">
			        <view v-if='item.introduce' class="text-wrapper_3 flex-col">
			          <text class="text_7">推荐</text>
			        </view>
			        <view class="text-group_1 flex-row" :style="{marginTop:item.introduce || item.num==5?'0':'4.2vw'}">
			          <text class="cash">{{item.num}}</text><text style="font-size: 3vw;margin-top:1.6vw;margin-left:0.5vw">元</text>
			          
			        </view>
					<text v-if='item.extraCoin' class="text_9">送{{item.extraCoin}}Y币</text>
			        <view v-if='item.extraVip' class="text-wrapper_4 flex-col">
			          <text class="text_11">赠送会员</text>
			        </view>
					<view v-if='activeCash == item.num' class="image-wrapper_1 flex-row">
					  <image
					    class="label_1"
					    referrerpolicy="no-referrer"
					    src="/static/lanhu_chongzhidanchuang/SketchPng3a4c5a3d6358825b758cd4f1c71149ab72ae599806e0f13d6b86dbd95bcb459f.png"
					  />
					</view>
			      </view>
			     
			      
			      <text class="text_23">推荐</text>
			    </view>
			    <view class="text-wrapper_7 flex-row">
			      <text class="text_24">支付方式：</text>
			    </view>
			    <view class="section_4 flex-row justify-between">
			      
				  <view class="box_3 flex-row justify-between" @click="payMethod='alipay'":class="payMethod=='alipay'?'activeBox3':''">
				    <image
				      class="label_3"
				      referrerpolicy="no-referrer"
				      src="/static/lanhu_chongzhidanchuang/SketchPngbbcc6f3b0b51306e0307703fc1c0dba52b4afa8851e224a51fab78fb52f15ff7.png"
				    />
				    <view class="image-text_3 flex-row justify-between">
				      <text class="text-group_6">支付宝</text>
				      <image
						v-if='payMethod=="alipay"'
				        class="label_4"
				        referrerpolicy="no-referrer"
				        src="/static/lanhu_chongzhidanchuang/SketchPng3a4c5a3d6358825b758cd4f1c71149ab72ae599806e0f13d6b86dbd95bcb459f.png"
				      />
				    </view>
				  </view>
			      <view class="box_3 flex-row justify-between" @click="payMethod='weChat'" :class="payMethod=='weChat'?'activeBox3':''">
			        <image
			          class="label_3"
			          referrerpolicy="no-referrer"
			          src="/static/lanhu_chongzhidanchuang/SketchPng3a3ec16850503d4e67730a72a5a2b84b592358668d96a9c9c5166405ebf83471.png"
			        />
			        <view class="image-text_3 flex-row justify-between">
			          <text class="text-group_6">微信支付</text>
			          <image
					  v-if='payMethod=="weChat"'
			            class="label_4"
			            referrerpolicy="no-referrer"
			            src="/static/lanhu_chongzhidanchuang/SketchPng3a4c5a3d6358825b758cd4f1c71149ab72ae599806e0f13d6b86dbd95bcb459f.png"
			          />
			        </view>
			      </view>
			    </view>
			    <view class="section_5 flex-row">
			      <view class="text-group_7 flex-col">
			        <text class="text_25">会员说明：</text>
			        <view class="text-wrapper_8">
			          <text class="paragraph_1">
						⑴ 会员专属分类里面的查询永久免费 
			          </text>
					  <br/>
					  <text class="paragraph_1">
					  	⑵ 会员专属客服鸭哥每天8时-23时在线，任何问题请及时咨询鸭哥，保证不翻车 
					  </text>
					  <br/>
					  <text class="paragraph_1">
					  	⑶ 会员永久有效，不限制时间，充值成功后不支持退款
					  </text>
			        </view>
			      </view>
			    </view>
			    <view class="section_6 flex-row">
			      <view class="text-wrapper_9 flex-col">
			        <text class="text_28">确认充值</text>
			      </view>
			    </view>
			  </view>
			  <view class="image-wrapper_2 flex-col">
			    <image
			      class="image_1"
			      referrerpolicy="no-referrer"
			      src="/static/lanhu_chongzhidanchuang/1898949cffe34a02a83e12f07524fa8d_mergeImage.png"
				  @click='close'
			    />
			  </view>
			  <view class="group_6 flex-col">
			    <view class="text-group_8 flex-col">
			      <text class="text_29">2017年12月21日上线&nbsp;&nbsp;至今{{day}}天</text>
			      <text class="text_30">查询数据安全加密</text>
			      <text class="text_31">鸭哥8-23时在线解答</text>
			    </view>
			    <view class="text-wrapper_10 flex-col">
			      <text class="text_32">
			        鸭宝查询&nbsp;&nbsp;只为做好专业查询一件事
			      </text>
			    </view>
			  </view>
			</view>
	
		</uni-popup>

</template>
<script>
export default {
	name:'Chongzhi',
  data() {
    return {
		activeCash:5,
		payMethod:'weChat',
		day:0,
      cashList:[
		  {
			  num:5,
			  extraCoin:0,
			  extraVip:false,
			  introduce:false
		  },
		  {
		  			  num:10,
		  			  extraCoin:3,
		  			  extraVip:true,
		  			  introduce:true
		  },
		  {
		  			  num:50,
		  			  extraCoin:20,
		  			  extraVip:true,
		  			  introduce:false
		  },
		  {
		  			  num:100,
		  			  extraCoin:60,
		  			  extraVip:true,
		  			  introduce:false
		  },
		  {
		  			  num:200,
		  			  extraCoin:160,
		  			  extraVip:true,
		  			  introduce:false
		  },
		  {
		  			  num:500,
		  			  extraCoin:500,
		  			  extraVip:true,
		  			  introduce:false
		  },
		  {
		  			  num:1000,
		  			  extraCoin:1200,
		  			  extraVip:true,
		  			  introduce:false
		  },
		  {
		  			  num:2000,
		  			  extraCoin:3000,
		  			  extraVip:true,
		  			  introduce:false
		  },
		  {
		  			  num:5000,
		  			  extraCoin:7500,
		  			  extraVip:true,
		  			  introduce:false
		  },
	  ]
    };
  },
  computed:{
		
	gainCash(){
		return this.activeCash + this.cashList.find(v=>{
			return(v.num == this.activeCash)
		}).extraCoin
	},
	coinNum(){
		return (this.activeCash/this.gainCash).toFixed(2)
	}
  },
  mounted(){
	  this.day = this.getOffsetDays(Date.now(), (new Date(2017, 12, 21)).getTime());
  },
  methods: {
	open(){
	          // 通过组件定义的ref调用uni-popup方法 ,如果传入参数 ，type 属性将失效 ，仅支持 ['top','left','bottom','right','center']
		this.$refs.popup.open('bottom')
	},
	close(){
		this.$refs.popup.close();
	},
	getOffsetDays(time1, time2) {
	    var offsetTime = Math.abs(time1 - time2);
	    return Math.floor(offsetTime / (3600 * 24 * 1e3));
	}
  }
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.css';
</style>
