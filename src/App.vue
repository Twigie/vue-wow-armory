<template>
    <div>
      <armory 
        :character_info="{
          name: 'Twigie',
          class: 'Rogue',
          level: '45',
          faction: 'horde',
          race: 'Human',
          honor: 5465132,
          week_kills: 32998,
          total_kills: 5648945616,
          is_online: true,
          gear: {
            head_id: 22478,
            neck_id: 0,
            shoulder_id: 22479,
            back_id: 0,
            chest_id: 22476,
            body_id: 49,
            tabard_id: 0,
            wrists_id: 22483,
            hands_id: 22481,
            waist_id: 22482,
            legs_id: 22477,
            feet_id: 22480,
            finger1_id: 23060,
            finger2_id: 19138,
            trinket1_id: 0,
            trinket2_id: 0,
            mainhand_id: 22802,
            offhand_id: 21126,
            range_id: 2947
          }
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
