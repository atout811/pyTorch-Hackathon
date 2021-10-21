<template>
  <div class="container">
    <div class="chat-container"></div>
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
.container {
  height: 100vh;
  width: 100vw;
  /* margin: 10px; */
  background-color: #a0e7e5;
  border-radius: 25px;
}
.chat-container {
  height: 80vh;
  width: 100vw;
  /* margin: 10px; */
  background-color: #fbe7c6;
  border-radius: 25px;
}
</style>