<template>
  <button @click="increment">Counter</button>
  <div>{{ counter }}</div>
</template>

<script>
import { ref, onMounted, watch, computed } from "vue"
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

    const arrayOfEmojis = computed(() => {
      return Array.from(new Array(counter.value), () => props.emoji).join(" ")
    })

    return { counter, increment }
  },
}
</script>

<style></style>
