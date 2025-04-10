---
layout: inner_no_margin
---

[back](./)

<style>
  .texture-grid {
    display: grid;
    grid-template-columns: repeat(11, 200px);
    gap: 1px;
    margin: 0 auto;
    max-width: 2200px;
    border-collapse: collapse;
    background-color: rgba(0, 0, 0, 0.05); /* light lines around the whole grid */
  }
  .texture-grid > div {
    background-color: white;
    border: 1px solid rgba(0, 0, 0, 0.08); /* subtle row/column separators */
    padding: 10px;
    text-align: center;
  }
  .span-text-texture {
    grid-column: 1 / 4; /* spans columns 4 to 11 (remember: 12 is exclusive) */
    background-color: #f0f0f0;
    padding: 10px;
    font-weight: bold;
    text-align: center;
  }
  .span-text-models {
    grid-column: 4 / 12; /* spans columns 4 to 11 (remember: 12 is exclusive) */
    background-color: #f0f0f0;
    padding: 10px;
    font-weight: bold;
    text-align: center;
  }
</style>

<div class="texture-grid">

  <!-- Full-width header row -->
  <div class="span-text-texture"><strong>Original Texture</strong></div>
  <div class="span-text-models"><strong>Models</strong></div>

  <!-- Header Row -->
  <div><strong>Image</strong></div>
  <div><strong>Sound</strong></div>
  <div><strong>Things to pay attention to:</strong></div>
  <div><img src="./assets/img/bubbles_2.gif" alt="Bubbles" style="max-width: 100%;"></div>
  <div><img src="./assets/img/fire.gif" alt="Fire" style="max-width: 100%;"></div>
  <div><img src="./assets/img/keyboard.gif" alt="Keyboard" style="max-width: 100%;"></div>
  <div><img src="./assets/img/rain_2.gif" alt="Rain" style="max-width: 100%;"></div>
  <div><img src="./assets/img/river.gif" alt="River" style="max-width: 100%;"></div>
  <div><img src="./assets/img/shards.gif" alt="Shards" style="max-width: 100%;"></div>
  <div><img src="./assets/img/waterfall.gif" alt="Waterfall" style="max-width: 100%;"></div>
  <div><img src="./assets/img/wind.gif" alt="Wind" style="max-width: 100%;"></div>

  <!-- Row: Bubbles -->
  <div><img src="./assets/img/bubbles_2.gif" alt="Bubbles" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/bubbles_copy.mp3"></audio></div>
  <div>Effervescence, popping rhythm</div>
  <div><audio controls style="width: 180px;" style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/bubbles_to_wind.mp3"></audio></div>

  <!-- Row: Fire -->
  <div><img src="./assets/img/fire.gif" alt="Fire" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/fire.mp3"></audio></div>
  <div>Crackling dynamics, hiss</div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/fire_to_wind.mp3"></audio></div>

  <!-- Row: Keyboard -->
  <div><img src="./assets/img/keyboard.gif" alt="Keyboard" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/keyboard.mp3"></audio></div>
  <div>Rhythmic tapping, mechanical textures</div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/keyboard_to_wind.mp3"></audio></div>

  <!-- Row: Rain -->
  <div><img src="./assets/img/rain_2.gif" alt="Rain" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/rain.mp3"></audio></div>
  <div>Continuous droplets, subtle variations</div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/rain_to_wind.mp3"></audio></div>

  <!-- Row: River -->
  <div><img src="./assets/img/river.gif" alt="River" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/river.mp3"></audio></div>
  <div>Flowing motion, low-end texture</div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/river_to_wind.mp3"></audio></div>

  <!-- Row: Shards -->
  <div><img src="./assets/img/shards.gif" alt="Shards" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/shards.mp3"></audio></div>
  <div>Sharp transients, glassy clinks</div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/shards_to_wind.mp3"></audio></div>

  <!-- Row: Waterfall -->
  <div><img src="./assets/img/waterfall.gif" alt="Waterfall" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/waterfall.mp3"></audio></div>
  <div>Dense water texture, downward motion</div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/waterfall_to_wind.mp3"></audio></div>

  <!-- Row: Wind -->
  <div><img src="./assets/img/wind.gif" alt="Wind" style="max-width: 100%;"></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_resynthesis/wind.mp3"></audio></div>
  <div>Swirling, airy textures</div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_bubbles.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_fire.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_keyboard.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_rain.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_river.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_shards.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_waterfall.mp3"></audio></div>
  <div><audio controls style="width: 180px;" src="./assets/audios/texdsp_timbre_transfer/wind_to_wind.mp3"></audio></div>

</div>

