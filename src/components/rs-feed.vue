<template>
  <div class="rs-feed-wrapper">
    <div class="rs-feed-header">
      <div class="rs-feed-header-info">
        <h2 class="rs-feed-name">Новое обращение</h2>
        <p class="rs-feed-description">Тестовый демо-магазин №127, 27 авг 2018, 12:12</p>
      </div>
      <button class="rs-feed-header-close-button">Закрыть обращение</button>
    </div>
    <div class="rs-feed-content">
      <rs-feed-message
        message-type="outgoing"
        sender="Вы"
        message-time="27 авг 2018, 12:12"
        message-text="Добрый день! Скажите, сколько, в среднем, приходиться ждать ответ на обращение? И почему мои вопросы теперь справа?"
        :attach="{src: '#', title: 'Вопросительное выражение.jpg'}"
        :images="['/src/img/default_img.jpg', '/src/img/default_img.jpg', '/src/img/default_img.jpg']"
      />
      <rs-feed-message
        message-type="incoming"
        sender="Робот Roistat"
        message-time="27 авг 2018, 19:48"
        user-pic="/src/img/default_img.jpg"
        message-text="Спасибо за обращение! Среднее время ответа в рабочее время составляет 4 часа. Как только сотрудник службы поддержки ответит на ваш вопрос, вы получите уведомление по электронной почте."
      />
      <rs-feed-message
        message-type="outgoing"
        sender="Вы"
        message-time="27 авг 2018, 20:12"
        message-text="Понял, спасибо."
      />
      <rs-feed-message
        message-type="incoming"
        sender="Тимур Тагиев"
        message-time="28 авг 2018, 09:09"
        message-text="Доброе утро! получили ли вы ответ на свой вопрос?"
      />
      <rs-feed-message
        message-type="outgoing"
        sender="Вы"
        message-time="27 авг 2018, 12:12"
        message-text="Добрый день! Скажите, сколько, в среднем, приходиться ждать ответ на обращение? И почему мои вопросы теперь справа?"
      />
      <rs-feed-message
        message-type="incoming"
        sender="Робот Roistat"
        message-time="27 авг 2018, 19:48"
        message-text="Спасибо за обращение! Среднее время ответа в рабочее время составляет 4 часа. Как только сотрудник службы поддержки ответит на ваш вопрос, вы получите уведомление по электронной почте."
      />
      <rs-feed-message
        message-type="outgoing"
        sender="Вы"
        message-time="27 авг 2018, 20:12"
        message-text="Понял, спасибо."
      />
      <rs-feed-message
        message-type="incoming"
        sender="Тимур Тагиев"
        message-time="28 авг 2018, 09:09"
        message-text="Доброе утро! получили ли вы ответ на свой вопрос?"
      />
      <rs-feed-message
        message-type="outgoing"
        sender="Вы"
        message-time="27 авг 2018, 12:12"
        message-text="Добрый день! Скажите, сколько, в среднем, приходиться ждать ответ на обращение? И почему мои вопросы теперь справа?"
      />
      <rs-feed-message
        message-type="incoming"
        sender="Робот Roistat"
        message-time="27 авг 2018, 19:48"
        message-text="Спасибо за обращение! Среднее время ответа в рабочее время составляет 4 часа. Как только сотрудник службы поддержки ответит на ваш вопрос, вы получите уведомление по электронной почте."
      />
      <rs-feed-message
        message-type="outgoing"
        sender="Вы"
        message-time="27 авг 2018, 20:12"
        message-text="Понял, спасибо."
      />
      <rs-feed-message
        message-type="incoming"
        sender="Тимур Тагиев"
        message-time="28 авг 2018, 09:09"
        message-text="Доброе утро! получили ли вы ответ на свой вопрос?"
      />
    </div>
    <div class="rs-feed-add-message">
      <textarea name="add-message-text" id="message-text" cols="30" rows="10" placeholder="Напиши ответ"></textarea>
      <div class="rs-feed-message-controls">
        <button class="add-message-send">Ответить</button>
        <button class="add-message-attach">Прикрепить файл</button>
      </div>
    </div>
  </div>
</template>

<script>
import RsFeedMessage from './rs-feed-message.vue';

export default {
  name: 'rs-feed',
  components: { RsFeedMessage },
  data() {
    return {};
  },
};
</script>

<style>
  * {
    margin: 0;
  }

  body, html {
    height: 100%;
  }

  .rs-feed-wrapper {
    width: 70%;
    height: 100%;
    float: right;
    display: flex;
    flex-direction: column;
    background-color: #f1f2f3;
  }

  .rs-feed-header {
    width: 100%;
    height: 72px;
    display: flex;
    flex-direction: row;
    padding: 16px 20px;
    align-items: center;
    justify-content: space-between;
    background-color: #fff;
    flex: 0 0 auto;
  }

  .rs-feed-header-info {
    width: 80%;
    display: flex;
    flex-direction: column;
  }

  .rs-feed-name {
    font-family: PT Sans Caption;
    font-style: normal;
    font-weight: bold;
    line-height: normal;
    font-size: 16px;
    color: rgba(27, 42, 48, 0.8);
  }

  .rs-feed-description {
    font-family: PT Sans;
    font-style: normal;
    font-weight: normal;
    line-height: normal;
    font-size: 12px;
    color: rgba(27, 42, 48, 0.6);
  }

  .rs-feed-header-close-button {
    height: 32px;
    background: linear-gradient(180deg, #FFFFFF 0%, #F1F2F3 100%);
    box-shadow: inset 0px 1px 0px rgba(27, 42, 48, 0.1), inset 0px -1px 0px rgba(27, 42, 48, 0.2), inset -1px 0px 0px rgba(27, 42, 48, 0.1), inset 1px 0px 0px rgba(27, 42, 48, 0.1);
    border-radius: 4px;
  }

  .rs-feed-content {
    flex: 1 1 auto;
    overflow: scroll;
    padding: 20px;
  }

  .rs-feed-add-message {
    padding: 0 20px;
    flex: 0 0 auto;
  }

  #message-text {
    width: 100%;
    height: 89px;
  }

  .rs-feed-message-controls {
    margin: 20px 0;
  }

  .rs-feed-message-controls button {
    height: 32px;
  }

  .add-message-send {
    background: #00A162;
    border-radius: 4px;
    color: white;
    margin-right: 16px;
  }

  .add-message-attach {
    background: linear-gradient(180deg, #FFFFFF 0%, #F1F2F3 100%);
    box-shadow: inset 0px 1px 0px rgba(27, 42, 48, 0.1), inset 0px -1px 0px rgba(27, 42, 48, 0.2), inset -1px 0px 0px rgba(27, 42, 48, 0.1), inset 1px 0px 0px rgba(27, 42, 48, 0.1);
    border-radius: 4px;
  }
</style>
