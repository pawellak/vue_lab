<template>
  <div class="display">
    <p class="label">Current Count</p>
    <p class="count-value">{{ store.count }}</p>
    <p class="double-info">Double: {{ store.doubleCount }}</p>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counterStore'

const store = useCounterStore()
</script>

<style scoped>
.display {
  background: #f5f5f5;
  border-radius: 12px;
  padding: 30px;
  margin-bottom: 30px;
}

.label {
  margin: 0 0 10px 0;
  color: #666;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: 600;
}

.count-value {
  margin: 0;
  font-size: 4rem;
  font-weight: 800;
  color: #667eea;
  line-height: 1;
}

.double-info {
  margin: 15px 0 0 0;
  color: #999;
  font-size: 0.9rem;
}
</style>
