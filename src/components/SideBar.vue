<template>
  <div class="q-pa-md">
    <q-list class="text-primary">
      <q-item
        to="/"
        clickable
        v-ripple
        :active="link === 'inbox'"
        @click="link = 'inbox'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="inbox" />
        </q-item-section>

        <q-item-section>Dashboard</q-item-section>
      </q-item>
      <q-separator spaced />
      <q-item
        to="/Client"
        clickable
        v-ripple
        :active="link === 'outbox'"
        @click="link = 'outbox'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="keyboard_command_key" />
        </q-item-section>

        <q-item-section>Client</q-item-section>
      </q-item>

      <q-item
        to="/Hotel"
        clickable
        v-ripple
        :active="link === 'trash'"
        @click="link = 'trash'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="fa-solid fa-hotel" />
        </q-item-section>

        <q-item-section>Hotel</q-item-section>
      </q-item>

      <q-item
        clickable
        v-ripple
        :active="link === 'settings'"
        @click="link = 'settings'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="location_city" />
        </q-item-section>

        <q-item-section>Ville</q-item-section>
      </q-item>

      <q-item
        clickable
        v-ripple
        :active="link === 'help'"
        @click="link = 'help'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="fa-solid fa-utensils" />
        </q-item-section>

        <q-item-section>Restaurant</q-item-section>
      </q-item>
      <q-item
        clickable
        v-ripple
        :active="link === 'taxi'"
        @click="link = 'taxi'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="fa-solid fa-taxi" />
        </q-item-section>

        <q-item-section>Agence Transport</q-item-section>
      </q-item>
      <q-item
        clickable
        v-ripple
        :active="link === 'marche'"
        @click="link = 'marche'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="fa-solid fa-store" />
        </q-item-section>

        <q-item-section>Marché</q-item-section>
      </q-item>
      <q-item
        clickable
        v-ripple
        :active="link === 'site'"
        @click="link = 'site'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="tour" />
        </q-item-section>

        <q-item-section>Site Touristique</q-item-section>
      </q-item>
      <q-separator spaced />
      <q-item
        clickable
        v-ripple
        :active="link === 'para'"
        @click="link = 'para'"
        active-class="my-menu-link"
      >
        <q-item-section avatar>
          <q-icon name="settings" />
        </q-item-section>

        <q-item-section>Parametres</q-item-section>
      </q-item>
    </q-list>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      link: ref("inbox"),
    };
  },
};
</script>

<style lang="sass">
.my-menu-link
  color: white
  background: #37aaf2
</style>
