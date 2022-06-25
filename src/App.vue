<template>
    <div>
      <armory 
        :character_info="{
          name: 'Twigie',
          class: 'Rogue',
          level: '45',
          faction: 'Alliance',
          race: 'Human',
          honor: 5465132,
          week_kills: 32998,
          total_kills: 5648945616,
        }"
      />
    </div>
</template>

<script setup>
import armory from './components/armory.vue'
</script>

<style>
html, body {
  margin: 0px !important;
  padding: 0px !important;
}
</style>
