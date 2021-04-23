<template>
  <button>Counter</button>
</template>

<script>
import { ref, onMounted } from "vue"
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

    const counter = ref(counter)
    const increment = () => counter.value++
    return {}
  },
}
</script>

<style></style>
