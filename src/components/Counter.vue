<template>
  <button>Counter</button>
</template>

<script>
export default {
  props: {
    emoji: {
      type: String,
      default: "💩",
    },
  },
  setup(props) {
    console.log(props.emoji)
    return {}
  },
}
</script>

<style></style>
