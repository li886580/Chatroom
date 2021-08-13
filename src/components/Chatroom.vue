<template>
  <div class="header">
    <p class="title">聊天室</p>
    <img src="../assets/icon/logout.svg" class="logout" title="登出" />
  </div>
  <div class="chatroomPage">
    <div class="sidebar">
      <div class="chatList">
        <div class="chatList__hall chatList__message">大廳</div>
        <div
          class="chatList__private chatList__message"
          v-for="privateMessage in privateMessages"
          :key="privateMessage.index"
        >
          <div class="name">{{ privateMessage.name }}</div>
          <div class="lastTime">{{ privateMessage.time }}</div>
          <div class="lastMessage">{{ privateMessage.lastMessage }}</div>
        </div>
      </div>
      <div class="search">
        <img class="search__icn" src="../assets/icon/search.svg" />
        <input class="search__input" type="text" placeholder="Search.." />
      </div>
    </div>
    <div class="dialog">
      <div class="dialog__box">
        <div
          class="message"
          v-for="message in messages"
          :key="message.index"
          v-bind:class="{
            'message--mySelf': message.accoundId !== 0 ? false : true,
          }"
        >
          <div
            class="message__name"
            v-bind:class="{
              'message__name--mySelf': message.accoundId !== 0 ? false : true,
            }"
          >
            {{ message.name }}
          </div>
          <div
            class="messageGroup"
            v-bind:class="{
              'messageGroup--mySelf': message.accoundId !== 0 ? false : true,
            }"
          >
            <div class="message__content">{{ message.content }}</div>
            <div
              class="message__time"
              v-bind:class="{
                'message__time--mySelf': message.accoundId !== 0 ? false : true,
              }"
            >
              {{ message.time }}
            </div>
          </div>
        </div>
      </div>
      <div class="sendMessage">
        <input
          class="sendMessage__input"
          type="text"
          placeholder="輸入訊息.."
        />
        <img class="sendMessage__icn" src="../assets/icon/send.svg" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Chatroom",
  data() {
    return {
      privateMessages: [
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "jeff", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "danny", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "平偉", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        {
          name: "mike",
          lastMessage: "哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦",
          time: "2021-08-12",
        },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
        { name: "mike", lastMessage: "哦哦哦哦哦", time: "2021-08-12" },
      ],
      messages: [
        {
          accoundId: 0,
          name: "mike",
          content: "哦哦哦哦哦哦哦哦哦哦",
          time: "2021-08-12",
        },
        {
          accoundId: 0,
          name: "mike",
          content: "哦哦哦哦哦",
          time: "2021-08-12",
        },
        {
          accoundId: 0,
          name: "mike",
          content: "哦哦哦哦哦",
          time: "2021-08-12",
        },
        {
          accoundId: 0,
          name: "mike",
          content: "哦哦哦哦哦",
          time: "2021-08-12",
        },
        {
          accoundId: 0,
          name: "mike",
          content:
            "哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦哦",
          time: "2021-08-12",
        },
        {
          accoundId: 1,
          name: "平偉",
          content: "公道價8萬1",
          time: "2021-08-12",
        },
        {
          accoundId: 2,
          name: "danny",
          content: "太貴了吧",
          time: "2021-08-12",
        },
        {
          accoundId: 2,
          name: "danny",
          content: "太貴了吧",
          time: "2021-08-12",
        },
        {
          accoundId: 2,
          name: "danny",
          content: "太貴了吧",
          time: "2021-08-12",
        },
        {
          accoundId: 2,
          name: "danny",
          content: "太貴了吧",
          time: "2021-08-12",
        },
        {
          accoundId: 2,
          name: "danny",
          content: "太貴了吧",
          time: "2021-08-12",
        },
        {
          accoundId: 2,
          name: "danny",
          content: "太貴了吧",
          time: "08-12",
        },
        {
          accoundId: 0,
          name: "mike",
          content: "哦哦哦哦哦",
          time: "08-12",
        },
        {
          accoundId: 0,
          name: "mike",
          content: "哦哦哦哦哦",
          time: "02:47",
        },
      ],
    };
  },
};
</script>

<style scoped src="../assets/css/Chatroom.css">
</style>