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
  padding: 0;
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