<template>
  <div id="wrapper">
    <div class="center">
      {{ character_info.name }}
      <div class="center title">Level {{ character_info.level }} {{ character_info.race}} {{ character_info.class }}</div>
    </div>
    <section id="armory">
      <section id="armory_left">
        <div class="item"><a href="https://classic.wowhead.com/item=22005" target="_blank"></a>
          <div><img src="../assets/default/head.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=" target="_blank"></a>
          <div><img src="../assets/default/neck.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=" target="_blank"></a>
          <div><img src="../assets/default/shoulders.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=22654" target="_blank"></a>
          <div><img src="../assets/default/chest.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=16905" target="_blank"></a>
          <div><img src="../assets/default/chest.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=" target="_blank"></a>
          <div><img src="../assets/default/body.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=" target="_blank"></a>
          <div><img src="../assets/default/tabard.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=" target="_blank"></a>
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
                    <td>Yes</td>
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
        <div class="item"><a href="https://classic.wowhead.com/item=22654" target="_blank"></a>
          <div><img src="../assets/default/hands.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=16910" target="_blank"></a>
          <div><img src="../assets/default/waist.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=22654" target="_blank"></a>
          <div><img src="../assets/default/legs.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=16906" target="_blank"></a>
          <div><img src="../assets/default/feet.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=" target="_blank"></a>
          <div><img src="../assets/default/finger.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=22654" target="_blank"></a>
          <div><img src="../assets/default/finger.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=22654" target="_blank"></a>
          <div><img src="../assets/default/trinket.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=19954" target="_blank"></a>
          <div><img src="../assets/default/trinket.gif" alt=""></div>
        </div>
      </section>

      <section id="armory_bottom">
        <div class="item"><a href="https://classic.wowhead.com/item=19352" target="_blank"></a>
          <div><img src="../assets/default/mainhand.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=22654" target="_blank"></a>
          <div><img src="../assets/default/offhand.gif" alt=""></div>
        </div>
        <div class="item"><a href="https://classic.wowhead.com/item=17069" target="_blank"></a>
          <div><img src="../assets/default/ranged.gif" alt=""></div>
        </div>
      </section>
    </section>
  </div>
</template>

<script setup>
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
  background-image: url('../assets/horde.png');
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

#armory_stats_top a {
  color:#ccc;
  font-size:14px;
  margin-right:20px;
  margin-left:20px;
}

#armory_stats a:hover {
  color:#fff;
}

.armory_current_tab {
  font-weight:bold;
  color:#fff !important;
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

#armory_stats_next a {
  border:1px solid #3a3a3a;
  background-image: linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -o-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -moz-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -webkit-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -ms-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    color-stop(1, rgba(255,255,255,0.3)),
    color-stop(0, rgba(200,200,200,0.3))
  );
  text-shadow:1px 1px 0px #000;
  box-shadow:0px 1px 0px #a2a2a2 inset;
  -webkit-box-shadow:0px 1px 0px #a2a2a2 inset;
  -moz-box-shadow:0px 1px 0px #a2a2a2 inset;
  color:#fff;

  width:80px;
  padding:3px;
  border-radius:5px;
  font-size:14px;
}

#armory_stats_next a:active {
  box-shadow:0px 0px 5px #151515 inset;
  -webkit-box-shadow:0px 0px 5px #151515 inset;
  -moz-box-shadow:0px 0px 5px #151515 inset;
  color:#c1c1c1;
}

#armory_stats_next {
  margin-top:10px;
}

#armory_stats td:first-child {
  color:#fff;
}

#armory_stats td:nth-child(2) {
  text-align:right;
}#armory_stats {
  float:left;
  width:367px;
  height:232px;
  margin-left:58px;
  margin-top:145px;
  text-shadow:1px 1px 0px #000;
  overflow:hidden;
}

#armory_stats_top a {
  color:#ccc;
  font-size:14px;
  margin-right:20px;
  margin-left:20px;
}

#armory_stats a:hover {
  color:#fff;
}

.armory_current_tab {
  font-weight:bold;
  color:#fff !important;
}

#armory_stats section {
  display:none;
  color:#fff;
  margin-top:8px;
}

#armory_stats td {
  padding:2%;
  font-size:14px;
}

#armory_stats table {
  margin-left:auto;
  margin-right:auto;
}

#armory_stats_next a {
  border:1px solid #3a3a3a;
  background-image: linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -o-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -moz-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -webkit-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -ms-linear-gradient(bottom, rgba(200,200,200,0.3) 0%, rgba(255,255,255,0.3) 100%);
  background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    color-stop(1, rgba(255,255,255,0.3)),
    color-stop(0, rgba(200,200,200,0.3))
  );
  text-shadow:1px 1px 0px #000;
  box-shadow:0px 1px 0px #a2a2a2 inset;
  -webkit-box-shadow:0px 1px 0px #a2a2a2 inset;
  -moz-box-shadow:0px 1px 0px #a2a2a2 inset;
  color:#fff;

  width:80px;
  padding:3px;
  border-radius:5px;
  font-size:14px;
}

#armory_stats_next a:active {
  box-shadow:0px 0px 5px #151515 inset;
  -webkit-box-shadow:0px 0px 5px #151515 inset;
  -moz-box-shadow:0px 0px 5px #151515 inset;
  color:#c1c1c1;
}

#armory_stats_next {
  margin-top:10px;
}

#armory_stats td:first-child {
  color:#fff;
}

#armory_stats td:nth-child(2) {
  text-align:right;
}
</style>
