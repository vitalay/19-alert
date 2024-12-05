<template>
  <div class="container">
    <app-alert
      v-if="alert"
      text="Это очень важное сообщение"
      title="Внимание"
      type="primary"
      closable
      @close="alert = false"
    ></app-alert>

    <div class="card">
      <button class="btn-primary" @click="toggleAlert">{{ alert ? 'Скрыть' : 'Показать' }} сообщение</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import AppAlert from './components/AppAlert.vue';

const alert = ref(false);

const toggleAlert = () => {
  alert.value = !alert.value;
};

</script>

<style scoped>
/* Ваши стили */
</style>
