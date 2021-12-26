<template lang="">
  <div>
    <div>
      <input type="text" v-model="inputValue" />
      <button @click="addItem">Adding</button>
    </div>
    <ul>
      <Listitem
        v-for="(value, index) in listArray"
        :key="index"
        :index="index"
        :style="style"
        :text="value === '' ? undefined : value"
        @delete = "catchDeleteItem"
      />
    </ul>
  </div>
</template>
<script>
import Listitem from "./ListItem.vue";
export default {
  // state
  data() {
    return {
      inputValue: "",
      listArray: [],
      style: {
        color: "pink",
      },
    };
  },

  components: {
    Listitem,
  },
  methods: {
    addItem() {
      this.listArray.push(this.inputValue);
      this.inputValue = "";
    },
    catchDeleteItem(index){
      this.listArray.splice(index,1)

    }
  },
};
</script>
<style lang=""></style>
