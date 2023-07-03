<template>
  <div>
    <!-- v-bind:하위컴포넌트에서 사용할(받을) props속성이름=”상위컴포넌트 즉, 데이터를 하위로 넘겨주는 상위 컴포넌트의 데이터 이름” -->
    <AppHeader :str="str"></AppHeader>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue"; // 파일의 내용을 AppHeader라는 변수에 담았다,
export default {
  data() {
    return {
      str: "st222",
    };
  },
  components: {
    // "app-header":AppHeader // 변수를 연결
    AppHeader,
  },
};
</script>

<style></style>
