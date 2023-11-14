<template>
  <view class="page flex-col">
    <view class="group_1 flex-row justify-between">
      <view class="box_1 flex-col">
        <image
          class="image_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_biaoqianlan/dae3a7fef9f0494c95f354e37310c976_mergeImage.png"
        />
        <text class="text_1">联系鸭哥</text>
      </view>
      <view class="box_2 flex-col">
        <image
          class="label_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_biaoqianlan/7eb78f6350d04db2a184bbb2a5c2bee5_mergeImage.png"
        />
        <text class="text_2">查验首页</text>
      </view>
      <view class="box_3 flex-col">
        <image
          class="label_2"
          referrerpolicy="no-referrer"
          src="/static/lanhu_biaoqianlan/SketchPng1996d68c62906ded8d449a15ab8f1b951759416dd1bb9effb38a142d051dda19.png"
        />
        <text class="text_3">会员中心</text>
      </view>
    </view>
    <view class="group_2 flex-row">
      <text class="text_4">安卓专区</text>
      <image
        class="image_2"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPngabb270719907028b76fb504dcf5c044f914f6527ab3bd580890c3756e7387a19.png"
      />
    </view>
    <view class="group_3 flex-row justify-between">
      <view class="group_4 flex-row">
        <view class="image-text_1 flex-col">
          <image
            class="image_3"
            referrerpolicy="no-referrer"
            src="/static/lanhu_biaoqianlan/SketchPngddb1ededffc4db723277efa6ac11ee05642e77d766055dcd7f488202fb348d23.png"
          />
          <text class="text-group_1">联系鸭哥</text>
        </view>
      </view>
      <view class="group_5 flex-row">
        <view class="image-text_2 flex-col">
          <image
            class="label_3"
            referrerpolicy="no-referrer"
            src="/static/lanhu_biaoqianlan/dba139c18254478c9c1ff73f58e092ef_mergeImage.png"
          />
          <text class="text-group_2">查验首页</text>
        </view>
      </view>
      <view class="group_6 flex-row">
        <view class="image-text_3 flex-col">
          <image
            class="image_4"
            referrerpolicy="no-referrer"
            src="/static/lanhu_biaoqianlan/b918205737864b2fb57144a55f3da4c7_mergeImage.png"
          />
          <text class="text-group_3">会员中心</text>
        </view>
      </view>
    </view>
    <view class="group_7 flex-row">
      <image
        class="label_4"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPngc4a7f048d419357a756dd449b702a496bc0153e4bd611a34e87ca659999081e3.png"
      />
      <image
        class="label_5"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
      />
      <image
        class="label_6"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPng479a038380f4eaec622541f64c6b4fd5e927704841de40232f7026da7bdd8da3.png"
      />
      <image
        class="label_7"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/88d28579671449f4913916944dc2af64_mergeImage.png"
      />
      <view class="image-wrapper_1 flex-col">
        <image
          class="label_8"
          referrerpolicy="no-referrer"
          src="/static/lanhu_biaoqianlan/SketchPngb9cec90a38f0a730c5310f1098e4885f7351da1f54a3bab8051baf8783d40acf.png"
        />
      </view>
      <image
        class="label_9"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPng29aa1d36cd24d4e87d3d8657eaccf60a0acf091af0695332af9b7e3c97bb3bd3.png"
      />
    </view>
    <view class="image-wrapper_2 flex-row">
      <image
        class="image_5"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPngee181d00598cd741bec00b0a071ce4393ab98a525189811875c08517e1d147f7.png"
      />
      <image
        class="label_10"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPng0e4867376a32990ce0e7a3c3df5c95b727b6b8271d04c4aba6840447bca22665.png"
      />
      <image
        class="label_11"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/e229cb5eb3934bfaa4856bc59d790bf1_mergeImage.png"
      />
      <image
        class="label_12"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPng6b792c672883d462a1b012b0d8e61e97017462e0329c2f699808dc97b115198f.png"
      />
      <image
        class="label_13"
        referrerpolicy="no-referrer"
        src="/static/lanhu_biaoqianlan/SketchPnga19ca7354b5c64af1ef3e39c8cab7e4369bde3efd3097b1d99a37ca684fdef84.png"
      />
    </view>
    <view class="group_8 flex-col">
      <view class="list_1 flex-row">
        <view
          class="image-text_4 flex-col"
          v-for="(item, index) in loopData0"
          :key="index"
        >
          <image
            class="label_14"
            referrerpolicy="no-referrer"
            :src="item.lanhuimage0"
          />
          <text
            class="text-group_4"
            :style="{ color: item.lanhufontColor0 }"
            v-html="item.lanhutext0"
          ></text>
        </view>
      </view>
    </view>
  </view>
</template>
<script>
export default {
  data() {
    return {
      loopData0: [
        {
          lanhuimage0:
            'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPng0071c8b96c0881423a42a19937216807d0bbd26b15f6e17f5c4987c0a33dd510',
          lanhutext0: '联系鸭哥',
          lanhufontColor0: 'rgba(25,31,37,0.4)'
        },
        {
          lanhuimage0:
            'https://lanhu-dds-backend.oss-cn-beijing.aliyuncs.com/merge_image/imgs/9c1728feaf984da4b07ee5d3a39bd433_mergeImage.png',
          lanhutext0: '查验首页',
          lanhufontColor0: 'rgba(0,0,0,1)'
        },
        {
          lanhuimage0:
            '/static/lanhu_biaoqianlan/SketchPng1996d68c62906ded8d449a15ab8f1b951759416dd1bb9effb38a142d051dda19.png',
          lanhutext0: '会员中心',
          lanhufontColor0: 'rgba(25,31,37,0.4)'
        }
      ],
      constants: {}
    };
  },
  methods: {}
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.rpx.css';
</style>
