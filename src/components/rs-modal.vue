<template>
  <div class="rs-modal-overlay" v-show="visible" @click="close">
    <div class="rs-modal" @click="handleModalClick">
      <div class="rs-modal-close" @click="close">
        X
      </div>

      <div v-if="$slots.hasOwnProperty('header')" class="rs-modal-header">
        <slot name="header" />
      </div>

      <div class="rs-modal-body">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: Boolean,
      default() {
        return false;
      },
    },
  },
  data() {
    return {
      visible: false,
    };
  },
  watch: {
    value: {
      immediate: true,
      handler(val) {
        this.visible = val;
      },
    },
    visible: {
      handler(val) {
        this.$emit('input', val);
      },
    },
  },
  methods: {
    close() {
      this.visible = false;
    },
    handleModalClick(e) {
      e.stopPropagation();
    },
  },
};
</script>

<style lang="less" scoped>
  .rs-modal {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    position: relative;
    background: #fff;
    border-radius: 4px;
    box-shadow: 0 6px 24px rgba(114, 125, 129, .75);

    &-overlay {
      background: rgba(0, 0, 0, 0.35);
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      z-index: 2000;

      display: flex;
      align-items: center;
      justify-content: center;
    }

    &-header {
      height: 40px;
      border-bottom: 1px solid #d7d8d9;
      padding: 0 40px 0 20px;

      display: flex;
      align-items: stretch;
    }

    &-body {
      padding: 10px 20px;
    }

    &-close {
      position: absolute;
      top: 0; right: 0;
      padding: 12px;
    }
  }
</style>
