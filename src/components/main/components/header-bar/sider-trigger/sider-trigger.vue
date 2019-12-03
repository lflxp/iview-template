<template>
  <Tooltip placement="bottom-start" theme="light">
    <a @click="handleChange" type="text" :class="['sider-trigger-a', collapsed ? 'collapsed' : '']"><Icon :type="icon" :size="size" /></a>
    <div slot="content" style="width: 666px;">
      <Button type="default" ghost>Default</Button>
      <Button type="primary" ghost>Primary</Button>
      <Button type="dashed" ghost>Dashed</Button>
      <Button type="text" ghost>Text</Button>
      <Button type="info" ghost>Info</Button>
      <Button type="success" ghost>Success</Button>
      <Button type="warning" ghost>Warning</Button>
      <Button type="error" ghost>Error</Button>
      <br/>
      <Button>Default</Button>
      <Button type="primary">Primary</Button>
      <Button type="dashed">Dashed</Button>
      <Button type="text">Text</Button>
      <br><br>
      <Button type="info">Info</Button>
      <Button type="success">Success</Button>
      <Button type="warning">Warning</Button>
      <Button type="error">Error</Button>
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
