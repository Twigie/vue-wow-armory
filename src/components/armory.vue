<template>
  <div id="wrapper">
    <div class="center">
      {{ character_info.name }}
      <div class="center title">Level {{ character_info.level }} {{ character_info.race}} {{ character_info.class }}</div>
    </div>
    <section id="armory" :style="{ 'background-image': 'url(/src/assets/' + character_info.faction + '.png)' }">
      <section id="armory_left">
        <div class="item" id="head"><a :href="wowhead_url + `${character_info.gear.head_id}`" target="_blank"></a>
          <div><img src="../assets/default/head.gif" alt=""></div>
        </div>
        <div class="item" id="neck"><a :href="wowhead_url + `${character_info.gear.neck_id}`" target="_blank"></a>
          <div><img src="../assets/default/neck.gif" alt=""></div>
        </div>
        <div class="item" id="shoulder"><a :href="wowhead_url + `${character_info.gear.shoulder_id}`" target="_blank"></a>
          <div><img src="../assets/default/shoulders.gif" alt=""></div>
        </div>
        <div class="item" id="back"><a :href="wowhead_url + `${character_info.gear.back_id}`" target="_blank"></a>
          <div><img src="../assets/default/back.gif" alt=""></div>
        </div>
        <div class="item" id="chest"><a :href="wowhead_url + `${character_info.gear.chest_id}`" target="_blank"></a>
          <div><img src="../assets/default/chest.gif" alt=""></div>
        </div>
        <div class="item" id="body"><a :href="wowhead_url + `${character_info.gear.body_id}`" target="_blank"></a>
          <div><img src="../assets/default/body.gif" alt=""></div>
        </div>
        <div class="item" id="tabard"><a :href="wowhead_url + `${character_info.gear.tabard_id}`" target="_blank"></a>
          <div><img src="../assets/default/tabard.gif" alt=""></div>
        </div>
        <div class="item" id="wrists"><a :href="wowhead_url + `${character_info.gear.wrists_id}`" target="_blank"></a>
          <div><img src="../assets/default/wrists.gif" alt=""></div>
        </div>
      </section>
      <section id="armory_stats">
          <div class="center" id="armory_stats_top">
          <b style="color: white;">Player Stats</b>
          </div>
          <section id="tab_stats" style="display:block;">
            <div style="width:1200px;height:194px;" id="attributes_wrapper">
              <div id="tab_armory_1" style="float:left;">
                <table width="367px">
                  <tr>
                    <td>Name</td>
                    <td>{{ character_info.name }}</td>
                  </tr>
                  <tr>
                    <td>Online</td>
                    <td v-if="character_info.is_online">Yes</td>
                    <td v-else>No</td>
                  </tr>
                  <tr>
                    <td>Honor Points</td>
                    <td>{{ character_info.honor }}</td>
                  </tr>
                  <tr>
                    <td>Last Week Kills</td>
                    <td>{{ character_info.week_kills }}</td>
                  </tr>
                  <tr>
                    <td>Total Kills</td>
                    <td>{{ character_info.total_kills }}</td>
                  </tr>

          </table>

    
        </div>
        </div>
          </section>
          </section>
      <section id="armory_right">
        <div class="item" id="hands"><a :href="wowhead_url + `${character_info.gear.hands_id}`" target="_blank"></a>
          <div><img src="../assets/default/hands.gif" alt=""></div>
        </div>
        <div class="item" id="waist"><a :href="wowhead_url + `${character_info.gear.waist_id}`" target="_blank"></a>
          <div><img src="../assets/default/waist.gif" alt=""></div>
        </div>
        <div class="item" id="legs"><a :href="wowhead_url + `${character_info.gear.legs_id}`" target="_blank"></a>
          <div><img src="../assets/default/legs.gif" alt=""></div>
        </div>
        <div class="item" id="feet"><a :href="wowhead_url + `${character_info.gear.feet_id}`" target="_blank"></a>
          <div><img src="../assets/default/feet.gif" alt=""></div>
        </div>
        <div class="item" id="finger1"><a :href="wowhead_url + `${character_info.gear.finger1_id}`" target="_blank"></a>
          <div><img src="../assets/default/finger.gif" alt=""></div>
        </div>
        <div class="item" id="finger2"><a :href="wowhead_url + `${character_info.gear.finger2_id}`" target="_blank"></a>
          <div><img src="../assets/default/finger.gif" alt=""></div>
        </div>
        <div class="item" id="trinket1"><a :href="wowhead_url + `${character_info.gear.trinket1_id}`" target="_blank"></a>
          <div><img src="../assets/default/trinket.gif" alt=""></div>
        </div>
        <div class="item" id="trinket2"><a :href="wowhead_url + `${character_info.gear.trinket2_id}`" target="_blank"></a>
          <div><img src="../assets/default/trinket.gif" alt=""></div>
        </div>
      </section>

      <section id="armory_bottom">
        <div class="item" id="mainhand"><a :href="wowhead_url + `${character_info.gear.mainhand_id}`" target="_blank"></a>
          <div><img src="../assets/default/mainhand.gif" alt=""></div>
        </div>
        <div class="item" id="offhand"><a :href="wowhead_url + `${character_info.gear.offhand_id}`" target="_blank"></a>
          <div><img src="../assets/default/offhand.gif" alt=""></div>
        </div>
        <div class="item" id="ranged"><a :href="wowhead_url + `${character_info.gear.range_id}`" target="_blank"></a>
          <div><img src="../assets/default/ranged.gif" alt=""></div>
        </div>
      </section>
    </section>
  </div>
</template>

<script setup>
  const wowhead_url = "https://classic.wowhead.com/item="
  const props = defineProps({
    character_info: {
      name: String,
      class: String,
      level: Number,
      faction: String,
      race: String,
      honor: Number,
      week_kills: Number,
      total_kills: Number,
      is_online: Boolean,
      gear: {
        head_id: Number,
        neck_id: Number,
        shoulder_id: Number,
        back_id: Number,
        chest_id: Number,
        body_id: Number,
        tabard_id: Number,
        wrists_id: Number,
        hands_id: Number,
        waist_id: Number,
        legs_id: Number,
        feet_id: Number,
        finger1_id: Number,
        finger2_id: Number,
        trinket1_id: Number,
        trinket2_id: Number,
        mainhand_id: Number,
        offhand_id: Number,
        range_id: Number
      }
    }
  })
</script>

<style scoped>

#wrapper {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.title {
  color: #deb601;
}

.center {
  text-align: center;
}

.item {
  width:70px;
  height:70px;
}

.item a {
  background-image:url('../assets/item_frame.png');
  width:68px;
  height:68px;
  margin-top:-6px;
  margin-left:-6px;
  position:absolute;
  z-index:999;
  display:block;
}

#armory {
  width:698px;
  margin-left:auto;
  margin-right:auto;
  min-height:512px;
  background-position:top center;
  background-repeat:no-repeat;
}

#armory_left {
  float:left;
  margin-left:40px;
  margin-top:15px;
  width:68px;
}

#armory_right {
  float:left;
  margin-top:15px;
  margin-left:65px;
  width:70px;
}

#armory_bottom .item {
  float:left;
}

#armory_bottom {
  clear:both;
  margin-left:auto;
  margin-right:auto;
  width:222px;
  height:70px;
  margin-top: 0px;
}
#armory_stats {
  float:left;
  width:367px;
  height:232px;
  margin-left:58px;
  margin-top:145px;
}


#armory_stats section {
  display:none;
  color:#fff;
  margin-top:8px;
}

#armory_stats table {
  margin-left:auto;
  margin-right:auto;
}

#armory_stats td:first-child {
  color:#fff;
}

#armory_stats td:nth-child(2) {
  text-align:right;
}
#armory_stats {
  float:left;
  width:367px;
  height:232px;
  margin-left:58px;
  margin-top:145px;
  overflow:hidden;
}
.armory_current_tab {
  font-weight:bold;
  color:#fff !important;
}
#armory_stats td {
  padding:2%;
  font-size:14px;
}

#armory_stats table {
  margin-left:auto;
  margin-right:auto;
}

#armory_stats_next {
  margin-top:10px;
}

</style>
