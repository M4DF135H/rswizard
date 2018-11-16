<template>
  <div class="rs-message-img-wrapper" @click="fullScreen = !fullScreen">
    <img class="rs-message-img" :src="src" alt="">
    <rs-modal :value="fullScreen">
      <img :src="src" alt="" style="height: 80vh;">
    </rs-modal>
  </div>
</template>

<script>
import RsModal from './rs-modal.vue';
export default {
  components: { RsModal },
  props: {
    src: String,
  },
  data() {
    return {
      fullScreen: false,
    };
  },
};
</script>

<style>
  .rs-message-img-wrapper {
    width: 100px;
    height: 100px;
    margin: 10px 10px 0 0;
    display: inline-flex;
    cursor: pointer;
  }
  .rs-message-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
</style>
