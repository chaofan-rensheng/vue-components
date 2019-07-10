<template>
  <div class="button-view container">
    <div class="title">不同类型按钮样式</div>
    <p-button size="default" type="primary">button</p-button>
    <p-button size="default" type="info">button</p-button>
    <p-button size="default" type="success">button</p-button>
    <p-button size="default" type="warning">button</p-button>
    <p-button size="default" type="error">button</p-button>

    <div class="title">不同大小的按钮样式</div>
    <p-button size="large" type="primary">button</p-button>
    <p-button size="default" type="primary"> button</p-button>
    <p-button size="small" type="primary">button</p-button>

    <div class="title">不同边框的按钮样式</div>
    <p-button border="solid">button</p-button>
    <p-button border="dashed">button</p-button>
    <p-button border="none">button</p-button>

    <p-button type='primary' :disabled="true">button</p-button>

    <div class="title">按钮组  水平方向的</div>
    <p-button-group size="large">
      <p-button type="primary">button</p-button>
      <p-button type="primary">button</p-button>
      <p-button type="primary">button</p-button>
      <p-button type="primary">button</p-button>
    </p-button-group>

    <div class="title">按钮组  垂直方向</div>
    <p-button-group size="large" :vertical="true">
      <p-button type="primary">button</p-button>
      <p-button type="primary">button</p-button>
      <p-button type="primary">button</p-button>
      <p-button type="primary">button</p-button>
    </p-button-group>
  </div>
</template>

<script>
import PButton from '@/components/button/button'
import PButtonGroup from '@/components/button/button-group'
export default {
  name: 'button-view',
  components: {
    PButton,
    PButtonGroup
  },
  props: {

  },
  data () {
    return {

    }
  },
  computed: {

  },
  mounted () {

  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>

</style>
