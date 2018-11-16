<template>
  <div class="userpic-wrapper">
    <img class="userpic-image" v-if="src" :src="src" alt="user-avatar">
    <div class="userpic-plug" v-else>
      <span class="userpic-plug-name">{{ userpicPlug }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'userpic',
  props: {
    src: String,
    userName: String,
  },
  data() {
    return {};
  },
  computed: {
    userpicPlug() {
      let nameSplited = this.userName.split(' ');
      return nameSplited[0][0] + nameSplited[1][0];
    },
  },
};
</script>

<style>
  .userpic-wrapper {
    width: 43px;
    height: 40px;
    margin-right: 12px;
  }

  .userpic-image {
    width: 40px;
    height: 40px;
    border-radius: 50px;
    object-fit: cover;
  }

  .userpic-plug {
    width: 40px;
    height: 40px;
    border-radius: 50px;
    background: #E6F3FB;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .userpic-plug-name {
    font-family: PT Sans;
    font-style: normal;
    font-weight: bold;
    line-height: normal;
    font-size: 14px;
    text-align: center;
    color: #26A4F0;
    text-transform: capitalize;
  }
</style>
