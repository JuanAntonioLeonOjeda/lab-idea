<template>
  <span>
    <button @click="addLike">{{ text }}</button>
  </span>
</template>

<script>
export default {
  name: "ButtonComponent",
  props: {
    text: {
      type: String,
      required: true,
    },
    addLike: {
      type: Function,
    },
  },
};
</script>

<style lang="scss" scoped></style>
