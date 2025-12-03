<template>
  <div class="counter-container">
    <div class="counter-card">
      <h1 class="title">Hello App</h1>
      <DisplayCounter />
      <ButtonsCounter />
      <ButtonReset />
    </div>
  </div>
</template>

<script setup>
import DisplayCounter from './DisplayCounter.vue'
import ButtonsCounter from './ButtonsCounter.vue'
import ButtonReset from './ButtonReset.vue'

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
</style>
