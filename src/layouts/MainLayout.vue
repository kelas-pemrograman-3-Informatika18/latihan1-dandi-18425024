<template>
  <q-layout view="lHh Lpr lFf">
    <q-header unelevated>
      <q-toolbar class="bg-black">
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          RUMAH SAKIT COVID-19
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          SISTEM RUMAH SAKIT
        </q-item-label>
        <q-item clickable active-class="active" exact v-ripple :to="{ name: 'dasboard'}">
          <q-item-section avatar>
            <q-icon name="dasboard" />
          </q-item-section>

          <q-item-section>
            Dasboard
          </q-item-section>
          </q-item>
          <q-item clickable active-class="active" exact v-ripple :to="{ name: 'inputPasien'}">
          <q-item-section avatar>
            <q-icon name="input" />
          </q-item-section>

          <q-item-section>
            Input Pasien
          </q-item-section>
          </q-item>
      </q-list>
    </q-drawer>

    <q-page-container class="bg-grey-2">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
