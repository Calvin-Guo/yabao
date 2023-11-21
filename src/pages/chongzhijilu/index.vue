<template>
  <view class="page flex-col">
    <view class="group_1 flex-row justify-between">
      <text class="text_1">鸭宝查询&nbsp;手机验机鉴定…</text>
      <view class="image-wrapper_1 flex-row justify-between">
        <image
          class="image_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chongzhijilu/SketchPnga553a8c46964d2453f188c7e9e85839b5b44b4c97cbd16de7cc424a524718841.png"
        />
        <image
          class="label_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chongzhijilu/SketchPngb26488a473f0c772a7a57d0fa2ea72b9e915dd4929351907e6681ffff8b45a0e.png"
        />
      </view>
      <view class="image-wrapper_2 flex-col">
        <image
          class="thumbnail_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chongzhijilu/SketchPng986131f428a5819aacc9a128a68b88908ff3aab18834e69ca02b46011941c39a.png"
        />
      </view>
    </view>
    <view class="group_2 flex-col">
      <view class="box_1 flex-row justify-between">
        <image
          class="label_2"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chongzhijilu/SketchPngdd209c8d029b54a275b51346e2e0f980ec63cd4475e2efcdad34b9bde0ca0647.png"
        />
        <text class="text_2">返回首页</text>
      </view>
      <view class="box_2 flex-row">
        <text class="text_3">消费记录（近1年）</text>
        <image
          class="image_2"
          referrerpolicy="no-referrer"
          src="/static/lanhu_chongzhijilu/SketchPng63accdbfeeccd6737065aa343d8f847f6a327604d9bf889f7163e40ea45c194b.png"
        />
        <text class="text_4">充值记录</text>
      </view>
      <view class="box_3 flex-row"><view class="box_4 flex-col"></view></view>
    </view>
    <view class="group_3 flex-col">
      <view class="list_1 flex-col">
        <view
          class="list-items_1 flex-col"
          v-for="(item, index) in loopData0"
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
    <view class="group_4 flex-col">
      <view class="block_1 flex-row">
        <view class="block_2 flex-col"></view>
        <text class="text_9">没有更多了</text>
        <view class="block_3 flex-col"></view>
      </view>
    </view>
    <image
      class="image_4"
      referrerpolicy="no-referrer"
      src="/static/lanhu_chongzhijilu/SketchPng8d710f78fb1e054b3833373fe3356a0c402245b5a94041a79ef6067692fba9e1.png"
    />
  </view>
</template>
<script>
export default {
  data() {
    return {
      loopData0: [
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
  methods: {}
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.css';
</style>
