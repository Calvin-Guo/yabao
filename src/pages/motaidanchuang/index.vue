<template>
  <view class="page flex-col">
    <view class="group_1 flex-col">
      <view class="list_1 flex-col">
        <view
          class="list-items_1 flex-col"
          v-for="(item, index) in loopData0"
          :key="index"
        >
          <text class="text_1" v-html="item.lanhutext0"></text>
          <text class="text_2" v-html="item.lanhutext1"></text>
          <view class="section_1 flex-col"></view>
          <view v-if="item.slot3 === 3" class="section_2 flex-row">
            <text class="text_3">取消</text>
            <image
              class="image_1"
              referrerpolicy="no-referrer"
              src="/static/lanhu_motaidanchuang/SketchPng896c436ecd27a58fcb8fa809cf376edff93e2e658f599a884820fdc183e8d58f.png"
            />
            <text class="text_4">取消</text>
            <image
              class="image_2"
              referrerpolicy="no-referrer"
              src="/static/lanhu_motaidanchuang/SketchPng896c436ecd27a58fcb8fa809cf376edff93e2e658f599a884820fdc183e8d58f.png"
            />
            <text class="text_5">确定</text>
          </view>
          <view v-if="item.slot2 === 2" class="section_3 flex-row">
            <text class="text_6">取消</text>
            <image
              class="image_3"
              referrerpolicy="no-referrer"
              src="/static/lanhu_motaidanchuang/SketchPng896c436ecd27a58fcb8fa809cf376edff93e2e658f599a884820fdc183e8d58f.png"
            />
            <text class="text_7">确定</text>
          </view>
          <text v-if="item.slot1 === 1" class="text_8">确定</text>
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
          lanhutext0: '单按钮弹窗',
          lanhutext1:
            '文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位',
          slot1: 1
        },
        {
          lanhutext0: '双按钮弹窗',
          lanhutext1:
            '文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位',
          slot2: 2
        },
        {
          lanhutext0: '三按钮弹窗',
          lanhutext1:
            '文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位文字占位',
          slot3: 3
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
