<template>
    <q-page padding>
        <q-card flat>
            <q-card-section class="q-gutter-md">
                <div class="text-h5">inputPasien</div>
                <q-form
                @submit="onSubmit"
                @reset="onReset"
                class="q-mt-lg"
                >
                <div class="q-gutter-md">
                 <q-input label="NAME_PASIEN" v-model="NAME_PASIEN" filled :rules="[ val => val && val.length > 0 || 'Tolong Ketik NAME_PASIEN']"></q-input>
                 <q-input label="UMUR" v-model="UMUR" filled :rules="[ val => val && val.length > 0 || 'Tolong Ketik UMUR']"></q-input>
                 <q-input label="JENIS_KELAMIN" v-model="JENIS_KELAMIN" filled :rules="[ val => val && val.length > 0 || 'Tolong Ketik JENIS_KELAMIN']"></q-input>
                 <q-input label="TTL" v-model="TTL" filled :rules="[ val => val && val.length > 0 || 'Tolong Ketik TTL']"></q-input>
                 <q-input label="ALAMAT" v-model="ALAMAT" filled :rules="[ val => val && val.length > 0 || 'Tolong Ketik ALAMAT']"></q-input>
                 <q-input label="PENYAKIT" v-model="PENYAKIT" filled :rules="[ val => val && val.length > 0 || 'Tolong ketik PENYAKIT']"></q-input>
                 <q-btn type="submit" label="input" color="teal" unelevated></q-btn>
                 <q-btn type="reset" label="Reset" color="teal" flat unelevated></q-btn>
                 </div>
                </q-form>
            </q-card-section>
        </q-card>
    </q-page>
</template>
<script>
export default {
  data () {
    return {
      NAME_PASIEN: null,
      UMUR: null,
      JENIS_KELAMIN: null,
      TTL: null,
      ALAMAT: null,
      PENYAKIT: null
    }
  },
  methods: {
    onReset () {
      this.NAME_PASIEN = null
      this.UMUR = null
      this.JENIS_KELAMIN = null
      this.TTL = null
      this.ALAMAT = null
      this.PENYAKIT = null
    },
    onSubmit () {
      this.$q.notify({
        type: 'positive',
        message: 'Berhasil Input Pasien'
      })
      this.$router.push({ name: 'dashboard' })
    }
  }
}
</script>
