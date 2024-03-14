<template>
  <div>
    <h1>Olá, {{ nome }}</h1>
    <input type="text" v-model="nome" />
    <p v-if="nome.length > 10">Nome muito longo</p>
    <p v-else-if="nome.length < 5">Nome curto</p>
    <TabelaUsuario :usuarios="usuarios"/>
    <!-- <table>
      <thead>
        <tr>
          <td>Id</td>
          <td>Nome</td>
        </tr>
      </thead>
      <tbody>
        <tr v-for="usuario in usuarios" :key="usuario.id">
          <td>{{ usuario.id }}</td>
          <td>{{ usuario.nome }}</td>
        </tr>
      </tbody>
    </table> -->
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import TabelaUsuario from '@/components/TabelaUsuario.vue'

const nome = ref('Teste')
const usuarios = ref([
  { id: 1, nome: 'Admin' },
  { id: 2, nome: 'User' }
])
</script>
