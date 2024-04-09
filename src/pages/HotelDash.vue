
<template>
  <q-layout view="hHh lpR lFf">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title> Dashboard GestionTourism </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <!-- drawer content -->
      <SideBar />
    </q-drawer>

    <q-page-container>
      <div class="text-h4 q-pa-md">Dashboard Hotel</div>
    </q-page-container>
    <q-footer class="bg-transparent text-white">
      <q-tabs v-model="tab" class="text-primary">
        <q-route-tab to="/" name="Dashboard" icon="inbox" label="Dashboard" />
        <q-route-tab
          to="/Client"
          name="Client"
          icon="keyboard_command_key"
          label="Cient"
        />
        <q-route-tab name="Parametre" icon="settings" label="Paramètres" />
      </q-tabs>
    </q-footer>
  </q-layout>
</template>

<script>
import { ref } from "vue";
import SideBar from "src/components/SideBar.vue";

export default {
  components: { SideBar },
  setup() {
    const leftDrawerOpen = ref(false);

    return {
      tab: ref("mails"),
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
};
</script>
<style lang="scss">
@media screen and (min-width: 768px) {
  .q-footer {
    display: none;
  }
}
</style>
