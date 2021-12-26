<template lang="">
  <li>
    {{ text }}
    <button @click = itemDelete>Delete</button>
  </li>
</template>
<script>
export default {
  // props: ["text"]
  props: {
    index: {
        type:Number
    },
    text: {
      type: String,
      required: true,
      default: "Hi",
    },
  },
  methods: {
      itemDelete(){
          this.$emit('delete',this.index)
      }
  },
  //
};
</script>
<style lang=""></style>
