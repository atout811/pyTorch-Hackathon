<template>
  <div class="baba">
    <div class="container">
      <h1 class="title">Welcome to our Chatbot feel free to talk to him</h1>
      <div class="chat-container">
        <div class="messages">
          <div v-for="(message, i) in chat" :key="i" class="message">
            <div :class="message.from == 'bot' ? 'bot' : 'user'">
              <v-avatar class="avatar" color="indigo">
                <v-icon dark>
                  {{
                    message.from == "bot"
                      ? "mdi-robot-dead-outline"
                      : "mdi-account-circle"
                  }}
                </v-icon>
              </v-avatar>
              <div class="content">
                <div v-if="image">
                  <v-img max-height="150" max-width="250" :src="image"></v-img>
                </div>
                <div class="messg">{{ message.message }}</div>
              </div>
            </div>
          </div>
        </div>
        <div class="input-group">
          <v-text-field
            class="text-input"
            label="Type your text here"
            v-model="text"
          ></v-text-field>
          <v-file-input v-model="image" accept="image/*"></v-file-input>
          <v-btn @click="sendMessage" icon color="var(--v-primary-base)">
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
        { from: "bot", message: "how can I help u ?" },
        { from: "user", message: "this is message yohohohoho ?" },
        { from: "bot", message: "okay, bye " },
        { from: "bot", message: "btw feel fear on human" },
      ],
      text: "",
      image: false,
    };
  },
  methods: {
    sendMessage: function () {
      console.log(image);
      this.chat.push({ from: "user", message: this.text, image: this.image });
    },
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
.messages {
  overflow: scroll;
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
  margin: 10px;
}
.user {
  display: flex;
  align-items: center;
  flex-direction: row-reverse;
  margin: 10px;
}
.messg {
  margin: 8px;
}
</style>