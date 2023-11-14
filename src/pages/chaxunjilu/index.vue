<template>
  <view class="page flex-col">
    <view class="box_1 flex-row justify-between">
      <text class="text_1">鸭宝查询&nbsp;手机验机鉴定…</text>
      <view class="image-wrapper_1 flex-row justify-between">
        <image
          class="image_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chaxunjilu/SketchPnga553a8c46964d2453f188c7e9e85839b5b44b4c97cbd16de7cc424a524718841.png"
        />
        <image
          class="label_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chaxunjilu/SketchPngb26488a473f0c772a7a57d0fa2ea72b9e915dd4929351907e6681ffff8b45a0e.png"
        />
      </view>
    </view>
    <view class="box_2 flex-col">
      <view class="group_1 flex-row">
        <image
          class="label_2"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chaxunjilu/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
        />
        <text class="text_2">历史查询记录</text>
        <text class="text_3">返回首页</text>
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
            :style="{ background: item.lanhuBg3 }"
          >
            <image
              v-if="item.slot2 === 2"
              class="label_4"
              referrerpolicy="no-referrer"
              src="/static/lanhu_chaxunjilu/SketchPng3fb3339a8ca824b6d1503669c8f00fe7ef9d3af16e1e1ae31f926f818c02d181.png"
            />
            <image
              v-if="item.slot1 === 1"
              class="thumbnail_1"
              referrerpolicy="no-referrer"
              src="/static/lanhu_chaxunjilu/SketchPngd0e1741e1c6125c6b07250d7cc505dd87bcd77a0085038f71e33405571be5512.png"
            />
          </view>
        </view>
      </view>
      <view class="group_3 flex-col">
        <view class="group_4 flex-row justify-end">
          <view class="text-wrapper_2 flex-col">
            <text class="text_8">图片配图</text>
          </view>
          <view class="text-group_3 flex-col">
            <text class="text_9">查询内容的标题</text>
            <text class="text_10">C02G67CAQ05F</text>
            <text class="text_11">2022-02-15&nbsp;13:57:54</text>
          </view>
          <view class="image-wrapper_3 flex-col">
            <image
              class="thumbnail_2"
              referrerpolicy="no-referrer"
              src="/static/lanhu_chaxunjilu/SketchPngd0e1741e1c6125c6b07250d7cc505dd87bcd77a0085038f71e33405571be5512.png"
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
    <image
      class="image_2"
      referrerpolicy="no-referrer"
      src="/static/lanhu_chaxunjilu/SketchPng8d710f78fb1e054b3833373fe3356a0c402245b5a94041a79ef6067692fba9e1.png"
    />
  </view>
</template>
<script>
export default {
  data() {
    return {
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
