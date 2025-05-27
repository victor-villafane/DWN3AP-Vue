<script setup>
import { ref } from 'vue'
let showModal = ref(false)
const mostrarModal = () => (showModal.value = true)
const cerrarModal = () => (showModal.value = false)
</script>

<template>
  <div>
    <h1 class="animate__animated animate__shakeX">Listado</h1>
    <button @click="mostrarModal">Mostrar</button>
    <transition>
      <div v-if="showModal" class="modal-overlay">
        <div class="animate__animated animate__bounceIn">
          <h3>Confirmacion</h3>
          <button @click="cerrarModal">cerrar</button>
        </div>
      </div>
    </transition>
  </div>
</template>
