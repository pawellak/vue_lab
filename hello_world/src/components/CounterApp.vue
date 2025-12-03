<template>
  <div class="counter-container">
    <div class="counter-card">
      <h1 class="title">Hello App</h1>
      <div class="display">
        <p class="label">Current Count</p>
        <p class="count-value">{{ store.count }}</p>
        <p class="double-info">Double: {{ store.doubleCount }}</p>
      </div>

      <div class="buttons">
        <button class="btn btn-sub" @click="store.decrement">
          <span class="symbol">−</span> Sub
        </button>
        <button class="btn btn-add" @click="store.increment">
          <span class="symbol">+</span> Add
        </button>
      </div>

      <button class="btn btn-reset" @click="store.reset">Reset</button>
    </div>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counterStore'

const store = useCounterStore()
</script>

<style scoped>
.counter-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  padding: 20px;
}

.counter-card {
  background: white;
  border-radius: 20px;
  padding: 40px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
  text-align: center;
  min-width: 300px;
}

.title {
  margin: 0 0 30px 0;
  font-size: 2rem;
  color: #333;
  font-weight: 700;
}

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
