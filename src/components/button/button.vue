<template>
  <button :class="classes" :disabled="disabled">
    <span v-if="showSlot"><slot></slot></span>
  </button>
</template>

<script>
const prefixCls = 'p-btn'
export default {
  name: 'Button',
  components: {

  },
  props: {
    disabled: {
      type: Boolean,
      default: false
    },
    size: {
      type: String,
      default () {
        return this.$parent && this.$parent.size ? this.parentSize : 'default'
      },
      validator: (value) => {
        console.log(value)
        return ['large', 'small', 'default'].includes(value)
      }
    },
    type: {
      type: String,
      default: 'primary',
      validator: (value) => {
        return ['primary', 'info', 'success', 'error', 'warning', ''].includes(value)
      }
    },

    border: {
      type: String,
      default: '',
      validator: (value) => {
        return ['solid', 'none', 'dashed', ''].includes(value)
      }
    },

    shape: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      showSlot: true
    }
  },
  computed: {
    classes () {
      return [
        `${prefixCls}`,
        {
          [`${prefixCls}-${this.size}`]: this.size !== 'default',
          [`${prefixCls}-${this.border}`]: this.border !== '',
          [`${prefixCls}-${this.type}`]: this.type !== '',
          [`${prefixCls}-${this.shape}`]: this.shape !== '',
          [`${prefixCls}-icon-only`]: this.showSlot === false
        }
      ]
    }
  },
  mounted () {
    this.showSlot = this.$slots.default !== undefined
  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>
  @import '@/styles/components/button.scss';

</style>
