<template>
	<view class="page flex-col">
		<view class="group_2 flex-row">
			<view class="image-text_1 flex-row justify-between">
				<image
					class="image_1"
					referrerpolicy="no-referrer"
					src="/static/lanhu_shouye/banner.png"
				/>
			</view>
			<image
				class="label_1"
				referrerpolicy="no-referrer"
				src="/static/lanhu_shouye/SketchPngc4a7f048d419357a756dd449b702a496bc0153e4bd611a34e87ca659999081e3.png"
			/>
		</view>
		<!-- <view class="searchBar group_1 flex-row">
			<input type="text" />
			<view class="button ok">
				查询
			</view>	
			<view class="button cancel">
				取消
			</view>	
		</view>	 -->
		<view class="group_3 flex-col">
			<view class="text-wrapper_1 flex-row justify-between">
				<text class="text_2" :class='active=="查询鉴定"?"text-active":""' @click='active="查询鉴定";expand=false'>查询鉴定</text>
				<text class="text_3" :class='active=="黑白官解"?"text-active":""' @click='active="黑白官解";expand=false'>黑白官解</text>
				<text class="text_4" :class='active=="会员专属"?"text-active":""' @click='active="会员专属";expand=false'>会员专属</text>
			</view>
			<view class="image-wrapper_1 flex-row" :style="{marginLeft:active=='查询鉴定'?'6.8vw':(active=='黑白官解'?'38.8vw':'72vw')}">
				<image
					class="image_2"
					referrerpolicy="no-referrer"
					src="/static/lanhu_shouye/SketchPngd1ae811bcce8af893869919831dd82e4b613738c05735641094307fb5996ba5a.png"
				/>
			</view>
			
		</view>
		<view class="group_1">
			<view class="image-wrapper_2 flex-row">
				<image
					class="image_3"
					referrerpolicy="no-referrer"
					src="/static/lanhu_shouye/SketchPng11905dd256775d06bd0104dcc3a8512f489d825e38d365a7a7c16ded480d8d0f.png"
					:style="{marginLeft:active=='查询鉴定'?'11.8vw':(active=='黑白官解'?'43.8vw':'77vw')}"
				/>
			</view>
		</view>
		<view v-if='active!="会员专属"' class="group_4 flex-row  " :class="expand?'expand':''">
			<view v-if="active=='查询鉴定'" class="section_1 flex-row">
				<view class="image-text_2 flex-row justify-between">
					<image
						class="label_2"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPng883f027e61400f05f11ecb8070e4054007b0de7260e259c0320b17a9c2deb1dd.png"
					/>
					<text class="text-group_2">苹果</text>
				</view>
			</view>
			<view v-if="active=='查询鉴定'" class="section_2 flex-row">
				<view class="image-text_3 flex-row justify-between">
					<image
						class="label_3"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPng7329b6d11324d94572098b929fd0e780be84ef5431578264c012529fac7c1312.png"
					/>
					<text class="text-group_3">安卓</text>
				</view>
			</view>
			<view v-if="active=='查询鉴定'" class="section_3 flex-row">
				<view class="image-text_4 flex-row justify-between">
					<image
						class="label_4"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPng8689a094a7d4caa91a040e22f25a07f82143ed36b39dc610fc11f9f078d0fa0e.png"
					/>
					<text class="text-group_4">耳机</text>
				</view>
			</view>
			<view v-if="active=='查询鉴定'" class="section_4 flex-row">
				<view class="image-text_5 flex-row justify-between">
					<image
						class="label_5"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPngc588e3d12755e1453d09404a753e0b4940709ae53108c56f373c6ef10fc3f20a.png"
					/>
					<text class="text-group_5">笔记本</text>
				</view>
			</view>
			<view v-if="active=='黑白官解'" class="section_4 flex-row">
				<view class="image-text_5 flex-row justify-between">
					<image
						class="label_5"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPngc588e3d12755e1453d09404a753e0b4940709ae53108c56f373c6ef10fc3f20a.png"
					/>
					<text class="text-group_5">黑白名单查询</text>
				</view>
			</view>
			<view v-if="active=='黑白官解'" class="section_4 flex-row">
				<view class="image-text_5 flex-row justify-between">
					<image
						class="label_5"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPngc588e3d12755e1453d09404a753e0b4940709ae53108c56f373c6ef10fc3f20a.png"
					/>
					<text class="text-group_5">官解服务</text>
				</view>
			</view>
			<view class="image-wrapper_4 flex-col" :style="{top:expand?'42.5vw':'30.5vw'}" @click="expand=!expand">
				<image
					class="label_8"
					referrerpolicy="no-referrer"
					src="/static/lanhu_shouye/down.png"
					:style="{transform: expand?'rotate(180deg)':'rotate(0deg)'}"
					
				/>
			</view>
		</view>
		<view class="container scroll">
			<view  class=" search flex-col align-center" :style="{right:active=='查询鉴定'?0:active=='黑白官解'?'100vw':'200vw'}">
				
				<view class="group_5 flex-row">
					<text class="text_5">苹果专区</text>
					<image
						class="image_4"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPngabb270719907028b76fb504dcf5c044f914f6527ab3bd580890c3756e7387a19.png"
					/>
				</view>
				<view class="group_6 flex-row" @click='goDetail'>
					<view class="text-wrapper_2 flex-col">
						<text class="text_6">01</text>
					</view>
					<view class="text-group_6 flex-col">
						<text class="text_7">苹果基础查询</text>
						<text class="text_8">
							免费查询基础数据，精确鉴定请使用苹果GSX验机报告，支持苹果所有设备
						</text>
					</view>
					<text class="text_9">5.0</text>
					<view class="block_1 flex-col">
						<text class="text_10">Y币</text>
						<image
							class="image_5"
							referrerpolicy="no-referrer"
							src="/static/lanhu_shouye/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
						/>
					</view>
				</view>
				<view class="group_7 flex-row">
					<view class="text-wrapper_3 flex-col">
						<text class="text_11">02</text>
					</view>
					<view class="text-group_7 flex-col">
						<text class="text_12">苹果GSX验机报告（Pro）</text>
						<text class="text_13">
							免费查询基础数据，精确鉴定请使用苹果GSX验机报告，支持苹果所有设备
						</text>
					</view>
					<view class="box_1 flex-col">
						<view class="box_2 flex-row">
							<view class="image-text_6 flex-row justify-between">
								<text class="text-group_8">鸭哥推荐</text>
								<image
									class="label_6"
									referrerpolicy="no-referrer"
									src="/static/lanhu_shouye/SketchPng0e4867376a32990ce0e7a3c3df5c95b727b6b8271d04c4aba6840447bca22665.png"
								/>
							</view>
						</view>
						<view class="text-wrapper_4 flex-row justify-between">
							<text class="text_14">589.8</text>
							<text class="text_15">Y币</text>
						</view>
						<image
							class="image_6"
							referrerpolicy="no-referrer"
							src="/static/lanhu_shouye/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
						/>
					</view>
				</view>
				<view class="group_14 flex-row">
					<text class="text_26">安卓专区</text>
					<image
						class="image_9"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPngabb270719907028b76fb504dcf5c044f914f6527ab3bd580890c3756e7387a19.png"
					/>
				</view>
				<view class="group_7 flex-row">
					<view class="text-wrapper_3 flex-col">
						<text class="text_11">02</text>
					</view>
					<view class="text-group_7 flex-col">
						<text class="text_12">苹果GSX验机报告（Pro）</text>
						<text class="text_13">
							免费查询基础数据，精确鉴定请使用苹果GSX验机报告，支持苹果所有设备
						</text>
					</view>
					<view class="box_1 flex-col">
						<view class="box_2 flex-row">
							<view class="image-text_6 flex-row justify-between">
								<text class="text-group_8">鸭哥推荐</text>
								<image
									class="label_6"
									referrerpolicy="no-referrer"
									src="/static/lanhu_shouye/SketchPng0e4867376a32990ce0e7a3c3df5c95b727b6b8271d04c4aba6840447bca22665.png"
								/>
							</view>
						</view>
						<view class="text-wrapper_4 flex-row justify-between">
							<text class="text_14">589.8</text>
							<text class="text_15">Y币</text>
						</view>
						<image
							class="image_6"
							referrerpolicy="no-referrer"
							src="/static/lanhu_shouye/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
						/>
					</view>
				</view>
				<view class="group_7 flex-row">
					<view class="text-wrapper_3 flex-col">
						<text class="text_11">02</text>
					</view>
					<view class="text-group_7 flex-col">
						<text class="text_12">苹果GSX验机报告（Pro）</text>
						<text class="text_13">
							免费查询基础数据，精确鉴定请使用苹果GSX验机报告，支持苹果所有设备
						</text>
					</view>
					<view class="box_1 flex-col">
						<view class="box_2 flex-row">
							<view class="image-text_6 flex-row justify-between">
								<text class="text-group_8">鸭哥推荐</text>
								<image
									class="label_6"
									referrerpolicy="no-referrer"
									src="/static/lanhu_shouye/SketchPng0e4867376a32990ce0e7a3c3df5c95b727b6b8271d04c4aba6840447bca22665.png"
								/>
							</view>
						</view>
						<view class="text-wrapper_4 flex-row justify-between">
							<text class="text_14">589.8</text>
							<text class="text_15">Y币</text>
						</view>
						<image
							class="image_6"
							referrerpolicy="no-referrer"
							src="/static/lanhu_shouye/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
						/>
					</view>
				</view>
				<view class="group_7 flex-row">
					<view class="text-wrapper_3 flex-col">
						<text class="text_11">02</text>
					</view>
					<view class="text-group_7 flex-col">
						<text class="text_12">苹果GSX验机报告（Pro）</text>
						<text class="text_13">
							免费查询基础数据，精确鉴定请使用苹果GSX验机报告，支持苹果所有设备
						</text>
					</view>
					<view class="box_1 flex-col">
						<view class="box_2 flex-row">
							<view class="image-text_6 flex-row justify-between">
								<text class="text-group_8">鸭哥推荐</text>
								<image
									class="label_6"
									referrerpolicy="no-referrer"
									src="/static/lanhu_shouye/SketchPng0e4867376a32990ce0e7a3c3df5c95b727b6b8271d04c4aba6840447bca22665.png"
								/>
							</view>
						</view>
						<view class="text-wrapper_4 flex-row justify-between">
							<text class="text_14">589.8</text>
							<text class="text_15">Y币</text>
						</view>
						<image
							class="image_6"
							referrerpolicy="no-referrer"
							src="/static/lanhu_shouye/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
						/>
					</view>
				</view>
				
			</view>
			<view  class="scroll unlock flex-col align-center" :style="{right:active=='黑白官解'?0:active=='会员专属'?'100vw':'-100vw'}">
				<view class="group_5 flex-row">
					<text class="text_5">查询黑白名单</text>
					<image
						class="image_4"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPngabb270719907028b76fb504dcf5c044f914f6527ab3bd580890c3756e7387a19.png"
					/>
				</view>
				<view class="group_7 flex-row">
					<view class="text-wrapper_3 flex-col">
						<text class="text_11">02</text>
					</view>
					<view class="text-group_7 flex-col">
						<text class="text_12">T版黑白名单查询</text>
						<text class="text_13">
							美国ATT运营商内查询此IMEI是否黑白名单，是否支持官解
						</text>
					</view>
					<view class="box_1 flex-col">
						
						<view class="text-wrapper_4 flex-row justify-between">
							<text class="text_14">589.8</text>
							<text class="text_15">Y币</text>
						</view>
						<image
							class="image_6"
							referrerpolicy="no-referrer"
							src="/static/lanhu_shouye/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
						/>
					</view>
				</view>
				<view class="group_5 flex-row">
					<text class="text_5">官解服务</text>
					<image
						class="image_4"
						referrerpolicy="no-referrer"
						src="/static/lanhu_shouye/SketchPngabb270719907028b76fb504dcf5c044f914f6527ab3bd580890c3756e7387a19.png"
					/>
				</view>
				<view class="group_7 flex-row">
					<view class="text-wrapper_3 flex-col">
						<text class="text_11">02</text>
					</view>
					<view class="text-group_7 flex-col">
						<text class="text_12">T版官解服务</text>
						<text class="text_13">
							T版官解服务
						</text>
					</view>
					<view class="box_1 flex-col">
						
						<view class="text-wrapper_4 flex-row justify-between">
							<text class="text_14">589.8</text>
							<text class="text_15">Y币</text>
						</view>
						<image
							class="image_6"
							referrerpolicy="no-referrer"
							src="/static/lanhu_shouye/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
						/>
					</view>
				</view>
			</view>
			<view  class="scroll vip flex-col align-center" :style="{left:active=='会员专属'?0:'100vw'}">
				会员专属
			</view>
		
		
			
		</view>
		
		
		
		<view v-if="!expand" class="group_16 flex-col"></view>
		
		
		<view class="shadow" :class="expand?'shdow-expand':''">
			
		</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
				
				constants: {},
				active:'查询鉴定',
				expand:false
			};
		},
		methods: {
			navigate:(item)=>{
				if(item.lanhutext0 == '会员中心'){
					uni.navigateTo({
						url:"/pages/wode/index",
						animationType:'slide-in-right'
					})
				}
			},
				
			goDetail(){
				uni.navigateTo({
					url:"/pages/chaxunx2fdancichaxun/index"
				})
			}
		},
	};
</script>
<style lang="css">
	@import "../common/common.css";
	@import "./assets/style/index.response.css";
</style>
