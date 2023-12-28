<template>
  <view class="page flex-col">
  
    <view class="group_1 flex-col">
      <view class="image-text_1 flex-row justify-between">
        <image
          class="image_1"
          referrerpolicy="no-referrer"
          src="/static/lanhu_denglu/SketchPngf5a58f1c94a4b5a4a2a06a27542b6ac6d05db3d922a6f753d55aa7d449a91b8b.png"
        />
        <text class="text-group_1">鸭宝查询</text>
      </view>
      <button class="button_1 flex-col" @click="onClick_1">
        <text class="text_1">登录</text>
      </button>
      <view class="image-wrapper_1 flex-row">
        <image
          class="icon_1"
          referrerpolicy="no-referrer"
          :src="item.lanhuimage0"
          v-for="(item, index) in loopData0"
          :key="index"
        />
      </view>
  
      <view class="group_2 flex-col">
        <view class="image-wrapper_2 flex-row justify-between">
          <image
            class="image_2"
            referrerpolicy="no-referrer"
            src="/static/lanhu_denglu/SketchPng626ba41d6c74d9c46d1c7f26f8a033ac2d5a741b9835d8b49e05346b4fe5e0fe.png"
          />
          <image
            class="image_3"
            referrerpolicy="no-referrer"
            src="/static/lanhu_denglu/SketchPng759155497cba7ed93d9a0aa82c1181b7422ad36b8c5811ad5a3d079e12fe6e19.png"
          />
          <image
            class="image_4"
            referrerpolicy="no-referrer"
            src="/static/lanhu_denglu/SketchPng49107f5602e50923b4db1192d1ab2ff6a8de57c8863875d834b3d41266f645df.png"
          />
        </view>
        <view class="section_1 flex-row">
          <text class="text_2">一键登录</text>
          <image
            class="image_5"
            referrerpolicy="no-referrer"
            src="/static/lanhu_denglu/SketchPngc1d65b179334df7676fa546d8264f03618ed4162d79a4e000a84e09297247b2a.png"
          />
        </view>
      </view>
      <image
        class="image_6"
        referrerpolicy="no-referrer"
        src="/static/lanhu_denglu/SketchPnge2fa576ec32015c022bd1c1c1dcb140a5d3f256dc7c7829cf04d1ff46c9007e0.png"
      />
      <view class="group_3 flex-col">
        <text class="text_3">请输入手机号码</text>
        <image
          class="image_7"
          referrerpolicy="no-referrer"
          src="/static/lanhu_denglu/SketchPngf3ef40aaae64b0cefe9949d5017d3e901875dd706dd9b65bba411f276245c829.png"
        />
        <view class="text-wrapper_1 flex-row justify-between">
          <text class="text_4">请输入短信验证码</text>
          <text class="text_5">获取验证码</text>
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
            'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPngd0178441ded02006a052a0275592b329fba2d4fb8d9de48b00467dc41fa458f5'
        },
        {
          lanhuimage0:
            'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPng05bc3e0e820eaefefb82294d67b401e94edcb0a5c89c23c0b7ca12a02a78a8bb'
        },
        {
          lanhuimage0:
            'https://lanhu.oss-cn-beijing.aliyuncs.com/SketchPng68a2b20ceb5d7c397182b7456bd524f50347a6586be32dd5a542273c6982f1de'
        }
      ],
      constants: {}
    };
  },
  methods: {
    onClick_1() {
      alert(1);
    }
  }
};
</script>
<style lang='css'>
@import '../common/common.css';
@import './assets/style/index.response.css';
</style>
