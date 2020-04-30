<template>
  <q-page padding>
    <q-table
      title="Data Rumah Sakit"
      :data="data"
      :columns="columns"
      row-key="name"
    >
      <template v-slot:body="props">
        <q-tr :props="props">
          <q-td key="NAME_PASIEN" :props="props">
            {{ props.row.NAME_PASIEN }}
          </q-td>
          <q-td key="UMUR" :props="props">
              {{ props.row.UMUR }}
          </q-td>
          <q-td key="JENIS_KELAMIN" :props="props">
              {{ props.row.JENIS_KELAMIN }}
          </q-td>
          <q-td key="TTL" :props="props">
              {{ props.row.TTL }}
          </q-td>
          <q-td key="ALAMAT" :props="props">>
              {{ props.row.ALAMAT }}
          </q-td>
          <q-td key="PENYAKIT" :props="props">
              {{ props.row.PENYAKIT }}
          </q-td>
        </q-tr>
      </template>
    </q-table>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      columns: [
        {
          name: 'NAME_PASIEN',
          required: true,
          label: 'NAME_PASIEN',
          align: 'left',
          field: 'NAME_PASIEN',
          sortable: true
        },
        { name: 'UMUR', align: 'center', label: 'UMUR', field: 'UMUR', sortable: true },
        { name: 'JENIS_KELAMIN', label: 'JENIS_KELAMIN', align: 'center', field: 'JENIS_KELAMIN', sortable: true },
        { name: 'TTL', label: 'TTL', field: 'TTL', align: 'center' },
        { name: 'ALAMAT', label: 'ALAMAT', field: 'ALAMAT', align: 'center' },
        { name: 'PENYAKIT', label: 'PENYAKIT', field: 'PENYAKIT', align: 'center' }
      ],
      data: [
        {
          NAME_PASIEN: 'DEWA',
          UMUR: '21',
          JENIS_KELAMIN: 'LAKI-LAKI',
          TTL: 'KOTA BUMI 01 JANUARI 1999',
          ALAMAT: 'BANDAR LAMPUNG',
          PENYAKIT: 'MERIANG'
        }
      ]
    }
  }
}
</script>
