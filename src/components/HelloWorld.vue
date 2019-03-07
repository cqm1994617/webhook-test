<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
}
.box {
  width: 800px;
  margin: 50px;
}
.title {
  color: #666;
  font-size: 18px;
  margin-bottom: 20px;
}
.remark {
  margin-top: 20px;
  margin-left: 40px;
  color: #999;
}
</style>

<template>
  <div class="container">
    <div
      class="box"
      v-for="item in data"
    >
      <h3 class="title">{{item.title}}</h3>
      <Steps :current="item.current">
        <Step 
          v-for="step in item.step" 
          :title="step.title">
        >
        </Step>
      </Steps>
      <div class="remark">{{item.remark}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      data: [
        {
          title: "招商撮合平台",
          step: [{
            title: '产品设计阶段',
            content: ''
          }, {
            title: 'demo阶段',
            content: ''
          }, {
            title: '开发阶段',
            content: ''
          }, {
            title: '测试阶段',
            content: ''
          }, {
            title: '发布',
            content: ''
          }],
          remark: '招商撮合还处于设计阶段，现在已有产品设计初稿，设计稿优化阶段持续时间约1-2周，下一阶段为产品demo阶段。',
          current: 0
        },
        {
          title: "数据印象",
          step: [{
            title: '产品设计阶段',
            content: ''
          }, {
            title: 'demo阶段',
            content: ''
          }, {
            title: '开发阶段',
            content: ''
          }, {
            title: '测试阶段',
            content: ''
          }, {
            title: '发布',
            content: ''
          }],
          remark: '数据印象还处于设计阶段，现在已有产品设计初稿，设计稿优化阶段持续时间约1-2周，下一阶段为产品demo阶段。',
          current: 0
        },
        {
          title: "大数据臻选",
          step: [{
            title: '产品设计阶段',
            content: ''
          }, {
            title: 'demo阶段',
            content: ''
          }, {
            title: '开发阶段',
            content: ''
          }, {
            title: '测试阶段',
            content: ''
          }, {
            title: '发布',
            content: ''
          }],
          remark: '大数据臻选还处于设计阶段，现在已有产品设计初稿，设计稿优化阶段持续时间约1-2周，下一阶段为产品demo阶段。',
          current: 0
        },
        {
          title: "智能客服",
          step: [{
            title: '产品设计阶段',
            content: ''
          }, {
            title: 'demo阶段',
            content: ''
          }, {
            title: '开发阶段',
            content: ''
          }, {
            title: '测试阶段',
            content: ''
          }, {
            title: '发布',
            content: ''
          }],
          remark: '智能客服还处于设计阶段，现在已有产品设计初稿，设计稿优化阶段持续时间约1-2周，下一阶段为产品demo阶段。',
          current: 0
        }
      ]
    };
  },
  props: {
    msg: String
  }
};
</script>
