
<template>
    <div class="alert" :class="type">
      <p class="alert-text">{{ title }}</p>
      <p>{{ text }}</p>
      <button class="btn" v-if="closable" @click="'close'">Закрыть</button>
    </div>
  </template>
  
  <script>
export default {
    
emits: ['close'],
props: {
  text: String,
  title: String,
  closable: {
    type: Boolean,
    required: false,
    default: false
  },
  type: {
    type: String,
    required: false,
    default: 'primary',
    validator(value) {
      return ['primary', 'danger', 'warning'].includes(value);
    }
  }
}

}
</script>
  
<style scoped>

</style>