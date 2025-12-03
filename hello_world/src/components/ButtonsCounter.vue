<template>
  <div class="buttons">
    <button class="btn btn-sub" @click="store.decrement">
      <span class="symbol">−</span> Sub
    </button>
    <button class="btn btn-add" @click="store.increment">
      <span class="symbol">+</span> Add
    </button>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counterStore'

const store = useCounterStore()
</script>

<style scoped>
.buttons {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-bottom: 15px;
  justify-content: center;
}

.btn {
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  gap: 6px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.symbol {
  font-size: 1.3rem;
  font-weight: 700;
}

.btn-sub {
  background: #ff6b6b;
  color: white;
  flex: 1;
}

.btn-sub:hover {
  background: #ff5252;
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(255, 107, 107, 0.4);
}

.btn-add {
  background: #51cf66;
  color: white;
  flex: 1;
}

.btn-add:hover {
  background: #40c057;
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(81, 207, 102, 0.4);
}
</style>
