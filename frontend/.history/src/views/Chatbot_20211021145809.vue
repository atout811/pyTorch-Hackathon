<template>
  <div class="baba">
    <div class="container">
      <div class="chat-container"></div>
      <h3>Welcome to our Chatbot feel free to talk to him</h3>
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
  align-items: flex-end;
}
.chat-container {
  height: 80%;
  width: 100%;
  /* margin: 10px; */
  background-color: #fbe7c6;
  border-radius: 25px;
}
</style>