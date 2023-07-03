<template>
  <header>
    <h1>Header {{ str }}</h1>
    <button @click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
  props: {
    str: String,
  },
  methods: {
    sendEvent() {
      // 상위 컴포넌트에 이벤트 연결(올리기)
      this.$emit("renew");
    },
  },
};
</script>

<style></style>
