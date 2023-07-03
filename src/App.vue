<template>
  <div>
    <!-- v-bind:하위컴포넌트에서 사용할(받을) props속성이름=”상위컴포넌트 즉, 데이터를 하위로 넘겨주는 상위 컴포넌트의 데이터 이름” -->
    <!-- 하위 컴포넌트에서 올린 이벤트 받기 =>emit / 받고 그것을 키로 넣어줌. 그리고 원하는 것을 바인딩 해서 넣어줌.-->
    <AppHeader :str="str" @renew="renewStr"></AppHeader>
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
  methods: {
    renewStr() {
      // str의 값을 바꾸기
      this.str = "Hi,, vue";
    },
  },
};
</script>

<style></style>
