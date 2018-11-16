<template>
  <div class="instruction instruction-wrapper">
    <h2 class="instruction-header">{{ header }}</h2>
    <div class="instruction-description">
      <p class="instruction-description-text">{{ description }}</p>
      <button class="instruction-next"
              @click="$emit('changeStep')"
              :disabled="value === max - 1">
        {{ button }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'rs-wizard-instruction',
  props: {
    id: Number,
    header: String,
    description: String,
    max: Number,
    button: {
      type: String,
      default: 'Далее',
    },
    value: Number,
  },
  data() {
    return {};
  },
};
</script>

<style>
  .instruction-wrapper {
    position: relative;
    display: flex;
    flex-direction: column;
    height: 100%;
    margin: 0 20px;
  }
  .instruction-header {
    margin-top: 20px;
    color: rgba(27, 42, 48, 0.8);
    font-family: PT Sans Caption;
    font-style: normal;
    font-weight: bold;
    line-height: normal;
    font-size: 14px;
  }
  .instruction-description {
    margin-top: 8px;
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 14px;
    color: rgba(27, 42, 48, 0.6);
    position: relative;
  }
  .instruction-description-text {
    margin-bottom: 60px;
  }
  .instruction-next {
    width: 92px;
    height: 32px;
    background-color: #00A162;
    border-radius: 4px;
    color: white;
    font-family: PT Sans;
    font-style: normal;
    font-weight: bold;
    line-height: normal;
    font-size: 14px;
    position: absolute;
    bottom: 20px;
    cursor: pointer;
  }
</style>
