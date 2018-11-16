<template>
  <div class="message" :class="[messageType === 'outgoing' ? 'message-outgoing' : 'message-incoming']">
    <rs-userpic v-if="messageType === 'incoming'" :src="userPic" :user-name="sender" />
    <div class="message-wrapper">
      <div class="message-info">
        <span class="message-info-sender">{{ sender }}, </span>
        <span class="message-info-time">{{ messageTime }}</span>
      </div>
      <div class="message-text">
        {{ messageText }}
      </div>

      <rs-feed-message-img v-for="(image, index) in images" :src="image" :key="index"/>
      <div class="message-attach" v-if="attach">
        <i class="far fa-paperclip"></i>
        <a class="message-attach-link" :href="attach.src" download>
          {{ attach.title }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import RsUserpic from './rs-userpic.vue';
import RsFeedMessageImg from './rs-feed-message-img.vue';

export default {
  components: { RsUserpic, RsFeedMessageImg },
  props: {
    messageType: String,
    sender: String,
    messageTime: String,
    messageText: String,
    userPic: String,
    attach: Object,
    images: Array,
  },
};
</script>

<style>
  .message {
    padding: 8px 12px;
    margin-bottom: 10px;
  }

  .message-outgoing {
    background: #F3FFE7;
    box-shadow: 0px 1px 1px rgba(27, 42, 57, 0.1);
    border-radius: 4px;
    width: 80%;
    float: right;
  }

  .message-incoming {
    width: 100%;
    background: #FFFFFF;
    box-shadow: 0px 1px 1px rgba(27, 42, 57, 0.1);
    border-radius: 4px;
    float: left;
    display: flex;
    flex-direction: row;
  }

  .message-wrapper {
    width: 100%;
  }

  .message-info {
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 12px;
    color: rgba(27, 42, 48, 0.6);
  }

  .message-text {
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 14px;
    color: rgba(27, 42, 48, 0.8);
    width: 60%;
    margin-top: 5px;
  }

  .message-attach {
    margin-top: 5px;
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 14px;
  }

  .message-attach-link {
    text-decoration: none;
    color: #0084D4;
  }
</style>
