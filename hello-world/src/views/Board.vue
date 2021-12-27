<template>
  <div class="board">
    {{boardName}} Board is coming soon!
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "Board",
  data() {
    return {
      boardName: "",
    };
  },
  created() {
      this.boardName = this.$route.params.id;
  }
};
</script>
