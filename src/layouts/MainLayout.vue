<style lang="sass">
.q-tab__label
  font-size: 20px
</style>
<template>
  <q-layout view="hHh lpR fff">
    <q-header class="bg-primary text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar size="70px">
            <q-icon name="dashboard" />
          </q-avatar>
          Dash Marketing Solutions
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs class="q-mb-md">
        <q-route-tab
          v-for="link in links"
          :to="link.path"
          :label="link.title"
          :key="link.path"
          exact
        />
      </q-tabs>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
<script setup>
const links = [
  { path: "/", title: "Home" },
  { path: "/pricing", title: "Pricing" },
  { path: "/careers", title: "Careers" },
  { path: "/about", title: "About" },
  { path: "/contacts", title: "Contacts" },
];
</script>
