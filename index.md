---
layout: inner
---

<div style="text-align: center">

<h1>A Statistics-Driven Differentiable Approach for Sound Textures Synthesis and Analysis</h1>

<p>
  <a href="https://cordutie.github.io/"><strong>Esteban Gutiérrez</strong></a><sup>1</sup>, 
  <a href="https://ffont.github.io/"><strong>Frederic Font</strong></a><sup>1</sup>, 
  <strong>Xavier Serra</strong>, and  
  <a href="https://lonce.org/"><strong>Lonce Wyse</strong></a><sup>1</sup>
</p>

<p><sup>1</sup> <em>Department of Information and Communications Technologies, Universitat Pompeu Fabra</em></p>

</div>

<div style="text-align: left; max-width: 800px; margin: 0 auto;">

<p>
This webpage provides supplementary materials for our paper <em>"A Statistics-Driven Differentiable Approach for Sound Textures Synthesis and Analysis"</em>, currently under review for the 25th edition of the Digital Audio Effects (DAFx) Conference.
</p>

<h2><strong>1. Introduction</strong></h2>

<p>
In this work we introduce <code>TexStat</code>, a perceptually grounded loss function inspired by McDermott and Simoncelli’s work. Alongside it, we present <code>TexEnv</code>, a lightweight differentiable synthesizer, and <code>TexDSP</code>, a DDSP-style generative model tailored for texture audio. All tools are open-source, implemented in PyTorch, and designed for efficient training and evaluation. Below are a few highlighted examples generated with <code>TexDSP</code>.
</p>

<div style="text-align: center">

  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
    <!-- Header row (Models and Sounds) -->
    <div style="font-weight: bold; text-align: center;"><strong>Model</strong></div>
    <div style="font-weight: bold; text-align: center;"><strong>Samples</strong></div>

  <!-- Fire Model Column -->
  <div style="text-align: center;">
    <img src="./assets/img/fire.gif" alt="Fire Model" style="max-width: 300px;"/>
  </div>
  <div>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/water_to_water.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio><br>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/fire_to_water.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio><br>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/fire_to_wind.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
  </div>

  <!-- Water Model Column -->
  <div style="text-align: center;">
    <img src="./assets/img/bubbles_2.gif" alt="Water Model" style="max-width: 300px;"/>
  </div>
  <div>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/water_to_fire.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio><br>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/water_to_water.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio><br>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/water_to_wind.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
  </div>

  <!-- Wind Model Column -->
  <div style="text-align: center;">
    <img src="./assets/img/rain.gif" alt="Wind Model" style="max-width: 300px;"/>
  </div>
  <div>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/wind_to_fire.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio><br>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/wind_to_water.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio><br>
    <audio controls style="max-width: 300px;">
      <source src="/assets/outputs/wind_to_wind.mp3" type="audio/mpeg">
      Your browser does not support the audio element.
    </audio>
  </div>
  </div>

</div>


<div style="margin-top: 20px;"></div>
<h2><strong>2. Models</strong></h2>

<h2><span style="font-weight: normal;">2.1. <code>TexStat</code> Loss</span></h2>
<p><code>TexStat</code> is a loss function based on a direct comparison of a revised version of <a href="https://doi.org/10.1016/j.neuron.2011.06.032" target="_blank" style="font-weight: normal;">McDermott and Simoncelli's summary of statistics</a>.  This approach allows the TexStat loss function to train texture sound generative models by focusing strictly on the statistical properties of sounds, rather than the sounds themselves. As a result, the synthesized textures naturally differ from the original inputs, while still preserving the essential perceptual qualities that define their type.</p>

<div style="margin-top: 20px;"></div>
<h2><span style="font-weight: normal;">2.2. TexEnv Synthesizer</span></h2>

<div style="margin-top: 20px;"></div>
<h2><span style="font-weight: normal;">2.3. TexDSP architecture</span></h2>

<div style="margin-top: 20px;"></div>
<h2><strong>3. Experiments</strong></h2>

<div style="margin-top: 20px;"></div>
<h2><span style="font-weight: normal;">3.1. TexStat Properties</span></h2>

<div style="margin-top: 20px;"></div>
<h2><span style="font-weight: normal;">3.2. TexStat Benchmarks</span></h2>

<div style="margin-top: 20px;"></div>
<h2><span style="font-weight: normal;">3.3. Summary Statistics as a Feature Vector</span></h2>

<div style="margin-top: 20px;"></div>
<h2><span style="font-weight: normal;">3.4. TexEnv Resynthesis</span></h2>

<div style="margin-top: 20px;"></div>
<h2><span style="font-weight: normal;">3.5. TexDSP models</span></h2>