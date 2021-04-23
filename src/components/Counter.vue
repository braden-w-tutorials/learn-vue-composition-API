<template>
  <button>Counter</button>
</template>

<script>
import { onMounted } from "@vue/runtime-core"
export default {
  props: {
    emoji: {
      type: String,
      default: "💩",
    },
  },
  setup(props) {
    console.log(props.emoji)
    onMounted(() => {
      console.log("Component mounted!")
    })
    return {}
  },
}
</script>

<style></style>
