<template>
  <Tooltip placement="bottom-start">
    <a @click="handleChange" type="text" :class="['sider-trigger-a', collapsed ? 'collapsed' : '']"><Icon :type="icon" :size="size" /></a>
    <div slot="content" style="width: 666px;">
      <p>子元素向左排列</p>
      <Row type="flex" justify="start" class="code-row-bg">
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
      </Row>
      <p>子元素向右排列</p>
      <Row type="flex" justify="end" class="code-row-bg">
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
      </Row>
      <p>子元素居中排列</p>
      <Row type="flex" justify="center" class="code-row-bg">
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
      </Row>
      <p>子元素等宽排列</p>
      <Row type="flex" justify="space-between" class="code-row-bg">
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
      </Row>
      <p>子元素分散排列</p>
      <Row type="flex" justify="space-around" class="code-row-bg">
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
          <Col span="4">col-4</Col>
      </Row>
    </div>
  </Tooltip>
</template>
<script>
export default {
  name: 'siderTrigger',
  props: {
    collapsed: Boolean,
    icon: {
      type: String,
      default: 'navicon-round'
    },
    size: {
      type: Number,
      default: 26
    }
  },
  methods: {
    handleChange () {
      this.$emit('on-change', !this.collapsed)
    }
  }
}
</script>
<style lang="less">
@import './sider-trigger.less';
</style>
