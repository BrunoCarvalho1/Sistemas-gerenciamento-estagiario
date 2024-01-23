<template>
  <q-page padding>
    <div class="row-12">
      <q-card class="my-card" bordered>
        <q-card-section >
          <div class="row">
            <q-btn class="col-2 q-mr-md" dense label="Novo estágiario" color="primary"/>
            <q-input class="q-ml-lg" dense style="width: 50%;" filled v-model="text" label="Pesquisar"></q-input>
          </div>
        </q-card-section>
        <q-table
        title="Lista de Usuários"
        :data="estagiarios"
        :columns="columns"
        row-key="id"
        :filter="searchText"
        />
      </q-card>
    </div>
  </q-page>
</template>

<script>
// import { defineComponent } from 'vue'

export default {
  MyList () {
    return {
      columns: [
        {
          name: 'name',
          label: 'Nome',
          field: 'name',
          align: 'left',
          sortable: true
        },
        {
          name: 'email',
          label: 'Email',
          field: 'email',
          align: 'left',
          sortable: true
        },
        {
          name: 'telefone',
          label: 'Telefone',
          field: 'telefone',
          align: 'left',
          sortable: true
        },
        {
          name: 'status',
          label: 'Status',
          field: 'status',
          align: 'left',
          sortable: true
        },
        {
          name: 'acoes',
          label: 'Ações',
          field: 'acoes',
          align: 'left',
          sortable: false
        }
      ],
    }
   }
  }

</script>
