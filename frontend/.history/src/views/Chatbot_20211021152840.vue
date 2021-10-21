<template>
  <div class="baba">
    <div class="container">
      <h1 class="title">Welcome to our Chatbot feel free to talk to him</h1>
      <div class="chat-container">
        <div v-for="(message, i) in chat" :key="i" class="messages">
          <div :class="message.from == 'bot' ? 'bot' : 'user'">
            <v-avatar color="indigo">
              <v-icon dark> mdi-account-circle </v-icon>
            </v-avatar>
            <div class="messg">this is a message yohohohohooh</div>
          </div>
        </div>
        <div class="input-group">
          <v-text-field
            class="text-input"
            label="Type your text here"
          ></v-text-field>
          <v-file-input accept="image/*"></v-file-input>
          <v-btn icon color="var(--v-primary-base)">
            <v-icon>mdi-send</v-icon>
          </v-btn>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "chatbot",
  data() {
    return {
      chat: [
        { from: "bot", message: "hey how can i help u ?" },
        { from: "user", message: "nohting" },
        { from: "bot", message: "okay, bye " },
        { from: "bot", message: "btw feel fear on human" },
      ],
    };
  },
};
</script>

<style>
.baba {
  height: 100vh;
  width: 100vw;
  display: flex;
}
.container {
  height: 70vh;
  width: 70vw;
  padding: 0;
  align-self: center;
  background-color: #a0e7e5;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
.title {
  margin: 10px;
  margin-top: 30px;
}
.chat-container {
  height: 80%;
  width: 100%;
  background-color: #fbe7c6;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 8px;
}
.text-input {
  width: 70%;
  margin: 5px;
}
.input-group {
  display: flex;
  align-items: center;
}
.bot {
  display: flex;
  align-items: center;
}
.user {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
.messg {
  margin-left: 8px;
}
</style>