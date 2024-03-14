<script setup lang="ts">
defineProps<{
  usuarios: { id: number; nome: string }[]
}>()
</script>

<template>
  <div>
    <table>
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
    </table>
    <!-- Seu código HTML aqui -->
  </div>
</template>
