# vue-wow-armory

A Vue Component of the Armory Module in https://github.com/vmangos/MadnessCMS

The component accepts the prop object character_info see below.

```javascript
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
```
## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
