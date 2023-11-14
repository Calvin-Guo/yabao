<template>
  <view class="page flex-col">
    <view class="box_1 flex-row justify-between">
      <text class="text_1">鸭宝查询&nbsp;手机验机鉴定…</text>
      <view class="image-wrapper_1 flex-row justify-between">
        <image
          class="image_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_xiaofeijilu/SketchPnga553a8c46964d2453f188c7e9e85839b5b44b4c97cbd16de7cc424a524718841.png"
        />
        <image
          class="label_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_xiaofeijilu/SketchPngb26488a473f0c772a7a57d0fa2ea72b9e915dd4929351907e6681ffff8b45a0e.png"
        />
      </view>
    </view>
    <view class="box_2 flex-col">
      <view class="group_1 flex-col">
        <view class="group_2 flex-row justify-between">
          <image
            class="label_2"
            referrerpolicy="no-referrer"
            src="/static/lanhu_xiaofeijilu/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
          />
          <text class="text_2">返回首页</text>
        </view>
        <view class="group_3 flex-row">
          <text class="text_3">消费记录（近1年）</text>
          <image
            class="image_2"
            referrerpolicy="no-referrer"
            src="/static/lanhu_xiaofeijilu/SketchPng63accdbfeeccd6737065aa343d8f847f6a327604d9bf889f7163e40ea45c194b.png"
          />
          <text class="text_4">充值记录</text>
        </view>
        <view class="group_4 flex-row">
          <view class="box_3 flex-col"></view>
        </view>
      </view>
      <view class="group_5 flex-row">
        <view class="text-group_1 flex-col">
          <text class="text_5">苹果SX验机报告（pro）报告报告报告报</text>
          <text class="text_6">2023-10-25&nbsp;17:50:23</text>
        </view>
        <image
          class="image_3"
          referrerpolicy="no-referrer"
          src="/static/lanhu_xiaofeijilu/SketchPngce4854b210f9e45e81895e2a9ef6dcef91e84788b33f5b6f7895d32c5d9e987a.png"
        />
        <text class="text_7">-50</text>
        <text class="text_8">币</text>
      </view>
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
    <image
      class="image_5"
      referrerpolicy="no-referrer"
      src="/static/lanhu_xiaofeijilu/SketchPng8d710f78fb1e054b3833373fe3356a0c402245b5a94041a79ef6067692fba9e1.png"
    />
  </view>
</template>
<script>
export default {
  data() {
    return {
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
