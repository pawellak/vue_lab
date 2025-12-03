<template>
  <button class="btn btn-reset" @click="store.reset">Reset</button>
</template>

<script setup>
import { useCounterStore } from '@/stores/counterStore'

const store = useCounterStore()
</script>

<style scoped>
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

.btn-reset {
  width: 100%;
  background: #868e96;
  color: white;
}

.btn-reset:hover {
  background: #748089;
  transform: translateY(-2px);
}

.btn:active {
  transform: translateY(0);
}
</style>
