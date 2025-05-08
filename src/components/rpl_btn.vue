<template>
  <button class="btn" @click="handleClick">
    <slot>Click</slot>
    <span
      v-for="(ripple, index) in ripples"
      :key="index"
      class="ripple"
      :style="{
        left: ripple.x + 'px',
        top: ripple.y + 'px',
        width: ripple.size + 'px',
        height: ripple.size + 'px',
      }"
    ></span>
  </button>
</template>

<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";

const props = defineProps({
  to: { type: String, default: null }, // optional route
  delay: { type: Number, default: 100 }, // delay before routing
});

const emit = defineEmits(["click"]);
const router = useRouter();
const ripples = ref([]);

function handleClick(event) {
  const button = event.currentTarget;
  const rect = button.getBoundingClientRect();
  const size = Math.max(rect.width, rect.height);
  const x = event.clientX - rect.left - size / 2;
  const y = event.clientY - rect.top - size / 2;

  const ripple = { x, y, size, id: Date.now() };
  ripples.value.push(ripple);

  setTimeout(() => {
    ripples.value = ripples.value.filter((r) => r.id !== ripple.id);
  }, 600);

  emit("click");

  if (props.to) {
    setTimeout(() => router.push(props.to), props.delay);
  }
}
</script>

<style scoped>
.btn {
  position: relative;
  border: none;
  outline: none;
  padding: 10px 30px;
  border-radius: 5px;
  font-size: 16px;
  font-weight: 500;
  cursor: pointer;
  overflow: hidden;
  font-family: "Raleway", sans-serif;
}

.ripple {
  position: absolute;
  background-color: rgba(255, 255, 255, 0.7);
  border-radius: 50%;
  transform: scale(0);
  animation: ripple 0.6s linear;
  pointer-events: none;
}

@keyframes ripple {
  to {
    transform: scale(4);
    opacity: 0;
  }
}
</style>
