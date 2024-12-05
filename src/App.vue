
<template>

<div class="container">
<app-alert 
text='Это очень важное сообщение'
title='Внимание'
type='warning'
closable="true"
></app-alert>

  <div class="card">
  
     <button class="btn-primary">Показать сообщение</button>

  </div>
</div>
 


 
</template>


<script setup>

import AppAlert from './components/AppAlert.vue'


  components: {
    AppAlert
  }


</script>



<style scoped>

</style>
