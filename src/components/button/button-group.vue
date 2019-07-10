<template>
  <div :class="classes">
    <slot>

    </slot>
  </div>
</template>

<script>
const prefixCls = 'p-btn-group'
export default {
  name: 'button-group',
  components: {

  },
  props: {
    size: {
      type: String,
      default: 'default',
      validator: (value) => {
        return ['small', 'default', 'large'].includes(value)
      }
    },

    // 水平方向 or  垂直方向
    vertical: {
      type: Boolean,
      default: false
    }
  },
  data () {
    return {

    }
  },
  computed: {
    classes () {
      return [
        `${prefixCls}`,
        {
          [`${prefixCls}-${this.size}`]: !!this.size,
          [`${prefixCls}-vertical`]: this.vertical
        }
      ]
    }
  },
  mounted () {

  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>
@import '@/styles/components/button.scss'
</style>
