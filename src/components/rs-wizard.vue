<template>
  <div class="rs-wizard">
    <div class="rs-wizard-header">
      <div class="rs-wizard-header-step" v-for="step in steps"
           :style="[(step.id - 1 < currentStep) ? {'cursor': 'pointer'} : {'cursor': 'default'}]"
           :key="step.id"
           :step_id="step.id - 1"
           :class="{ active: step.active }"
           @click="stepBackward">
        <span class="rs-wizard-header-step-index">
          {{ step.id }}
        </span>
        <span class="rs-wizard-header-step-name">
          {{ step.title }}
        </span>
      </div>
    </div>
    <div class="rs-wizard-step-content">
      <component v-for="step in steps"
                 :key="step.id"
                 :is="step.component"
                 :header="step.header"
                 :id="step.id"
                 :description="step.description"
                 @changeStep="currentStep < steps.length - 1 ? currentStep += 1 : currentStep"
                 v-show="step.active"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'rs-wizard',
  props: {
    steps: Array,
  },
  data() {
    return {
      currentStep: 0,
    };
  },
  watch: {
    currentStep(val, oldval) {
      let valDiff = -(val - oldval);

      if (val >= this.steps.length) {
        return;
      }

      if (oldval < val) {
        this.steps[val].active = true;
        this.steps[val - 1].active = false;
        this.steps[val - 1].complited = true;
      } else {
        this.steps[val].active = true;
        this.steps[val + valDiff].active = false;
        this.steps[val + valDiff].complited = true;
      }
    },
  },
  methods: {
    stepBackward(e) {
      let targetStep = parseInt(e.currentTarget.getAttribute('step_id'));

      if (targetStep < this.currentStep) {
        this.currentStep = targetStep;
      }
    },
  },
};
</script>

<style>
  .rs-wizard {
    width: 901px;
    height: 397px;
    box-shadow: 0px 1px 1px rgba(27, 42, 57, 0.1);
    border-radius: 2px;
    position: relative;
  }
  .rs-wizard-header {
    width: 100%;
    height: 40px;
    box-shadow: inset 0px -1px 0px rgba(27, 42, 48, 0.1);
    display: flex;
    flex-direction: row;
  }
  .rs-wizard-header-step {
    display: flex;
    align-items: center;
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 12px;
    color: rgba(27, 42, 48, 0.4);
    margin-left: 20px;
  }
  .rs-wizard-header-step-name {
    margin-left: 12px;
  }
  .rs-wizard-header-step:after {
    content: '>';
    width: 24px;
    height: 24px;
    line-height: 26px;
    font-size: 20px;
    margin-left: 20px;
    padding-left: 7px;
  }
  .rs-wizard-header-step:last-child:after {
    display: none;
  }
  .active {
    font-family: PT Sans;
    font-style: normal;
    line-height: normal;
    font-size: 12px;
    color: #00A162;
  }
  .active .rs-wizard-header-step-name {
    font-weight: bold;
  }
  .rs-wizard-step-content {
    width: 100%;
    max-height: 357px;
    height: 100%;
    position: relative;
    overflow: scroll;
  }
</style>
