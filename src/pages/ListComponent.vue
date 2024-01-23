<template>
  <q-page padding>
    <div class="row-12">
      <q-card class="my-card" bordered>
       <q-card-section v-if="!cadastro">
        <div class="row">
          <q-btn class="col-2 q-mr-md" dense label="+Novo Usuário" color="primary" @click="cadastrar"></q-btn>
          <q-input class="q-ml-lg" dense style="width: 50%;" label="Pesquisar usuário" filled></q-input>
          <q-table
            class="q-mt-lg"
            style="width: 1000%;"
            separator="cell"
            flat bordered
            title="Lista de usuários"
            :rows="rows"
            dense
            :columns="columns"
            row-key="name"
          />
        </div>

        </q-card-section>
       <q-card-section v-if="cadastro" class="text-h6">Novo cadastro
        <q-input class="q-ma-md" label="Nome" filled v-model="text"></q-input>
        <q-input class="q-ma-md" label="Telefone" filled v-model="text"></q-input>
        <q-input class="q-ma-md" label="Senha" filled v-model="text"></q-input>
        <q-input class="q-ma-md" label="Email" filled v-model="text"></q-input>
        <q-input class="q-ma-md" label="Status" filled v-model="text"></q-input>
        <q-input class="q-ma-md" label="Repetir" filled v-model="text"></q-input>
      </q-card-section>
      <div class="q-ma-md">
        <q-btn class="q-mr-sm" style="text-align: right;" color="primary" @click="cadastrar">Adicionar</q-btn>
        <q-btn style="text-align: right;" color="primary" @click="cadastrar">Cancelar</q-btn>
      </div>
      </q-card>
    </div>
  </q-page>
</template>

<script setup>

import { ref } from 'vue'

const cadastro = ref(false)
function cadastrar (){
  cadastro.value = !cadastro.value
  console.log(cadastro.value)
}
const columns = [
{
    name: 'nome',
    required: true,
    label: 'Nome',
    align: 'center',
    field: row => row.name,
    // format: val => `${val}`,
    sortable: true
  },
  { name: 'email', align: 'center', label: 'Email', field: 'email', sortable: true },
  { name: 'telefone', align: 'center', label: 'Telefone', field: 'telefone', sortable: true },
  { name: 'perfil', align: 'center', label: 'Perfil', field: 'perfil' },
  { name: 'status', align: 'center', label: 'Status', field: 'status' },
  { name: 'acoes', align: 'center', label: 'Ações', field: 'acoes' }
]
const rows = [
  {
    name: 'Bruno Santos Carvalho',
    email: 'brunobulhoes@outlook.com',
    telefone: '(73) 98145-5500',
    perfil: 'Admin',
    status: 'Ativo',
    acoes: ''
  },
  {
    name: 'Carlos Eduardo Souza Carvalho',
    email: 'carloseduardo@outlook.com',
    telefone: '(73) 98143-3494',
    perfil: 'Estágiario',
    status: 'Pendente',
    acoes: ''
  }
]


</script>
