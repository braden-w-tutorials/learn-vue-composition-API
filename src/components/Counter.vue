<template>
  <button @click="increment">Counter</button>
  <div>{{ counter }}</div>
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

    const counter = ref(0)
    const increment = () => counter.value++

    watch(
      () => counter,
      (newValue, oldValue) => {
        if (current === 5) {
          console.log("You have clicked five times!")
        }
      }
    )

    return { counter, increment }
  },
}
</script>

<style></style>
