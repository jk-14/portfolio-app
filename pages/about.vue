<script setup>
    const { data: apiData } = await useFetch('/api/count')
</script>

<template>
    <v-row class="ma-4">
        <p class="mb-2">This page will be displayed at the /about route.</p>
        <v-expansion-panels variant="accordion">
        <v-expansion-panel
            v-for="i in apiData.count"
            :key="i"
            :title="'Item'+i"
            text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        ></v-expansion-panel>
        </v-expansion-panels>
        <div class="mt-2">
            <NuxtLink to="/">Navigate to the Home page</NuxtLink>
        </div>
    </v-row>
  </template>