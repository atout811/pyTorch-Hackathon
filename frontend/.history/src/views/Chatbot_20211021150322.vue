<template>
  <div class="baba">
    <div class="container">
      <h1 class="title">Welcome to our Chatbot feel free to talk to him</h1>
      <div class="chat-container">
        <div class="messages"></div>
        <v-text-field
          class="text-input"
          label="Type your text here"
        ></v-text-field>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "chatbot",
  data() {
    return {
      chat: [],
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
  /* margin: 10px; */
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
  /* margin: 10px; */
  background-color: #fbe7c6;
  border-radius: 25px;
}
.text-input {
  width: 70%;
  margin: 5px;
}
</style>