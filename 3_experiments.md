<p>Several experiments were conducted to validate the ideas and models proposed in this work. The details regarding all these experiments can be found here.</p>
<!-- ---------------------------------------------------------------------------------------------------------------------------------------- -->
<div style="margin-top: 20px;"></div>
<details>
<summary><span style="font-weight: normal; font-size: 1.5em; color: black">3.1. TexStat Properties 📊</span></summary>

<p>
Two properties desirable in a loss function tailored for texture sounds are related to the stability under time shifting and addition of noise. In order to test these properties on the <code>TexStat</code> loss function, we compute the loss between a random selection of segments of sounds corresponding to the three categories of <a href="https://huggingface.co/datasets/cordutie/MicroTex" target="_blank" style="font-weight: normal;"><code>MicroTex</code></a> and their corresponding transformations using various parameters. The experiment was also run with the MSS loss for comparison and some of the results can be found in <strong>Tables 1 and 2</strong>. For further exploration see this article's webpage.
</p>

<div style="overflow-x: auto; max-width: 80%; margin: 0 auto; padding: 10px; box-sizing: border-box;">
  <table style="width: 100%; border-collapse: collapse; font-size: 0.9em;">
    <thead style="background-color: #f2f2f2;">
      <tr>
        <th style="border: 1px solid #ccc; padding: 8px;">Selection</th>
        <th style="border: 1px solid #ccc; padding: 8px;">Loss</th>
        <th style="border: 1px solid #ccc; padding: 8px;">10%</th>
        <th style="border: 1px solid #ccc; padding: 8px;">30%</th>
        <th style="border: 1px solid #ccc; padding: 8px;">50%</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>BOReilly</td><td><code>TexStat</code></td><td>0.12 ± 0.06</td><td>0.12 ± 0.06</td><td>0.12 ± 0.06</td></tr>
      <tr><td>BOReilly</td><td>MSS</td><td>5.34 ± 1.14</td><td>5.51 ± 1.29</td><td>5.58 ± 1.55</td></tr>
      <tr><td>Freesound</td><td><code>TexStat</code></td><td>0.04 ± 0.03</td><td>0.04 ± 0.03</td><td>0.04 ± 0.03</td></tr>
      <tr><td>Freesound</td><td>MSS</td><td>5.17 ± 1.24</td><td>5.26 ± 1.35</td><td>5.25 ± 1.34</td></tr>
      <tr><td>Syntex</td><td><code>TexStat</code></td><td>0.16 ± 0.11</td><td>0.16 ± 0.11</td><td>0.16 ± 0.11</td></tr>
      <tr><td>Syntex</td><td>MSS</td><td>10.52 ± 7.28</td><td>10.04 ± 6.62</td><td>9.45 ± 6.57</td></tr>
    </tbody>
  </table>
  <p style="text-align: center; font-size: 0.85em; color: #666;">
  <strong>Table 1.</strong> Time-Shift Robustness. Loss measurement between a sound and its time-shifted version. The amount of time shift is given in % of the total signal duration. Computed over 300 one-second sounds randomly sampled from the three main sources in the <code>MicroTex</code> dataset.
  </p>  
</div>

<div style="margin-top: 20px;"></div>

<div style="overflow-x: auto; max-width: 80%; margin: 0 auto; padding: 10px; box-sizing: border-box;">
  <table style="width: 100%; border-collapse: collapse; font-size: 0.9em;">
    <thead style="background-color: #f2f2f2;">
      <tr>
        <th style="border: 1px solid #ccc; padding: 8px;">Selection</th>
        <th style="border: 1px solid #ccc; padding: 8px;">Loss</th>
        <th style="border: 1px solid #ccc; padding: 8px;">10%</th>
        <th style="border: 1px solid #ccc; padding: 8px;">30%</th>
        <th style="border: 1px solid #ccc; padding: 8px;">50%</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>BOReilly</td><td><code>TexStat</code></td><td>0.12 ± 0.06</td><td>0.12 ± 0.06</td><td>0.12 ± 0.06</td></tr>
      <tr><td>BOReilly</td><td>MSS</td><td>5.34 ± 1.14</td><td>5.51 ± 1.29</td><td>5.58 ± 1.55</td></tr>
      <tr><td>Freesound</td><td><code>TexStat</code></td><td>0.04 ± 0.03</td><td>0.04 ± 0.03</td><td>0.04 ± 0.03</td></tr>
      <tr><td>Freesound</td><td>MSS</td><td>5.17 ± 1.24</td><td>5.26 ± 1.35</td><td>5.25 ± 1.34</td></tr>
      <tr><td>Syntex</td><td><code>TexStat</code></td><td>0.16 ± 0.11</td><td>0.16 ± 0.11</td><td>0.16 ± 0.11</td></tr>
      <tr><td>Syntex</td><td>MSS</td><td>10.52 ± 7.28</td><td>10.04 ± 6.62</td><td>9.45 ± 6.57</td></tr>
    </tbody>
  </table>
  <p style="text-align: center; font-size: 0.85em; color: #666;">
  <strong>Table 2.</strong> Noise-Addition Robustness. Loss measurement between a sound and its noisy version. The amount of noise added is given in % of the signal's energy. Same data sampling as in the previous experiment.
  </p>  
</div>

<p>
The results show that <code>TexStat</code> is highly stable with respect to both time shifting and noise addition, adding a penalty only in the category that had sounds that include silence (which generate instability since they have null standard deviance).
</p>

</details>
<!-- ---------------------------------------------------------------------------------------------------------------------------------------- -->
<div style="margin-top: 20px;"></div>
<details>
<summary><span style="font-weight: normal; font-size: 1.5em; color: black">3.2. TexStat Benchmarks 📊</span></summary>
<p>To benchmark the computational requirements of <code>TexStat</code>, we evaluated its computation time, gradient descent time, and GPU memory usage. These measurements were conducted multiple times, recording the time taken for loss computation and optimization while tracking memory allocation. The results are presented in Table 3, along with the values for other typical losses.</p>

<div style="overflow-x: auto; max-width: 80%; margin: 0 auto; padding: 10px; box-sizing: border-box;">
<table style="width: 100%; border-collapse: collapse; font-size: 0.9em;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th style="border: 1px solid #ccc; padding: 8px;">Loss</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Forward pass time (ms)</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Backward pass time (ms)</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Memory usage (MB)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>TexStat</code></td>
      <td>93.5 ± 0.4</td>
      <td>154.6 ± 0.4</td>
      <td>0.84 ± 2.5</td>
    </tr>
    <tr>
      <td>MSS</td>
      <td>3.9 ± 0.3</td>
      <td>8.5 ± 0.3</td>
      <td>0.85 ± 2.6</td>
    </tr>
    <tr>
      <td>MSE</td>
      <td>0.2 ± 0.3</td>
      <td>0.2 ± 0.1</td>
      <td>1.7 ± 5.0</td>
    </tr>
    <tr>
      <td>MAE</td>
      <td>0.1 ± 0.0</td>
      <td>0.2 ± 0.1</td>
      <td>0.8 ± 2.5</td>
    </tr>
  </tbody>
</table>
<p style="text-align: center; font-size: 0.85em; color: #666;">
  <strong>Table 3.</strong> Measurements regarding computation time, gradient computation time, and memory usage in batches of 32 signals of size 65,536 (around 1.5s at a sample rate of 44,100 Hz). The losses studied were <code>TexStat</code>, Multi-Scale Spectrogram (MSS), Mean Squared Error (MSE), and Mean Absolute Error (MAE). All measurements were done using CUDA on an RTX 4090 GPU.
</p>
</div>

<p>
The results show that, as expected, the <code>TexStat</code> loss function is slower than other less specific losses, but it uses a similar amount of memory.
</p>

</details>
<!-- ---------------------------------------------------------------------------------------------------------------------------------------- -->
<div style="margin-top: 20px;"></div>
<details>
<summary><span style="font-weight: normal; font-size: 1.5em; color: black">3.3. Summary Statistics as a Feature Vector 📊</span></summary>

<p>
To test <code>TexStat</code> summary statistics as a powerful representation suitable for evaluation metrics like FAD, we conducted the following experiment. First, all data in the three selections of the <code>MicroTex</code> dataset were segmented, and both their summary statistics and VGGish embeddings <a href="#ref-vggish">[VGGish]</a> were computed. Then, a downstream classifier (MLP with hidden layers 128 and 64) was trained for each case. A summary of the results is presented in Table 4.
</p>

<div style="overflow-x: auto; max-width: 80%; margin: 0 auto; padding: 10px; box-sizing: border-box;">
<table style="width: 100%; border-collapse: collapse; font-size: 0.9em;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th style="border: 1px solid #ccc; padding: 8px;">Model</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Selection</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Accuracy</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Precision</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Recall</th>
      <th style="border: 1px solid #ccc; padding: 8px;">F1</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><code>TexStat</code></td><td>BOReilly</td><td>0.94</td><td>0.94</td><td>0.94</td><td>0.94</td></tr>
    <tr><td>VGGish</td><td>BOReilly</td><td>0.71</td><td>0.73</td><td>0.71</td><td>0.71</td></tr>
    <tr><td><code>TexStat</code></td><td>Freesound</td><td>0.99</td><td>0.99</td><td>0.99</td><td>0.99</td></tr>
    <tr><td>VGGish</td><td>Freesound</td><td>0.98</td><td>0.99</td><td>0.98</td><td>0.98</td></tr>
    <tr><td><code>TexStat</code></td><td>Syntex</td><td>1.0</td><td>1.0</td><td>1.0</td><td>1.0</td></tr>
    <tr><td>VGGish</td><td>Syntex</td><td>0.95</td><td>0.95</td><td>0.95</td><td>0.94</td></tr>
  </tbody>
</table>
<p style="text-align: center; font-size: 0.85em; color: #666;">
  <strong>Table 4.</strong> Lorea.
</p>
</div>

<p>
The results indicate that, in the context of texture sounds, <code>TexStat</code> summary statistics are strictly more informative than general-purpose embeddings like VGGish.
</p>

</details>
<!-- ---------------------------------------------------------------------------------------------------------------------------------------- -->
<div style="margin-top: 20px;"></div>
<details>
<summary><span style="font-weight: normal; font-size: 1.5em; color: black">3.4. TexEnv Resynthesis 🎧</span></summary>
<p>
Extensive exploration using the <code>TexEnv</code> synthesizer in resynthesis tasks, employing a signal processing-based parameter extractor, was conducted to better understand its behavior and limitations. A summary of sound examples can be found on this article's page.
</p>

<p>
Some key findings:
<ul>
  <li>Water-like sounds (e.g., flowing water, rain, bubbling) benefited from <strong>larger filterbanks</strong> but not larger parameter sets.</li>
  <li>Crackling sounds (e.g., fireworks, bonfires) improved with <strong>larger parameter sets</strong> but were less sensitive to filterbank size.</li>
</ul>
These insights were used to determine the optimal parameters for model training.
</p>

</details>
<!-- ---------------------------------------------------------------------------------------------------------------------------------------- -->
<div style="margin-top: 20px;"></div>
<details>
<summary><span style="font-weight: normal; font-size: 1.5em; color: black">3.5. TexDSP models 🎧📊</span></summary>

<p>
To demonstrate the capabilities of <code>TexStat</code>, we trained a series of <code>TexDSP</code> models using different parameters, with <code>TexStat</code> as the sole loss function. Below are the training details for these models.
</p>

<div style="overflow-x: auto; max-width: 80%; margin: 0 auto; padding: 10px; box-sizing: border-box;">
<table style="width: 100%; border-collapse: collapse; font-size: 0.9em;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th style="border: 1px solid #ccc; padding: 8px;">Texture</th>
      <th style="border: 1px solid #ccc; padding: 8px;">$N_F$</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Enc/Dec Layers</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Params per Band</th>
      <th style="border: 1px solid #ccc; padding: 8px;">Frame Size (s)</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Bubbles</td><td>24</td><td>3/3</td><td>512</td><td>1.49</td></tr>
    <tr><td>Fire</td><td>16</td><td>3/3</td><td>256</td><td>0.74</td></tr>
    <tr><td>Keyboard</td><td>24</td><td>3/3</td><td>256</td><td>1.49</td></tr>
    <tr><td>Rain</td><td>24</td><td>1/3</td><td>512</td><td>1.49</td></tr>
    <tr><td>River</td><td>24</td><td>1/3</td><td>128</td><td>0.74</td></tr>
    <tr><td>Shards</td><td>32</td><td>3/3</td><td>512</td><td>1.49</td></tr>
    <tr><td>Waterfall</td><td>24</td><td>1/3</td><td>256</td><td>1.49</td></tr>
    <tr><td>Wind</td><td>24</td><td>1/3</td><td>256</td><td>1.49</td></tr>
  </tbody>
</table>
<p style="text-align: center; font-size: 0.85em; color: #666;">
  <strong>Table 5.</strong> Lorea.
</p>
</div>

<p style="font-size: 0.85em; color: #666;">
All encoders and decoders used 256 neurons per layer. All models used <code>$N_G = 6$</code> and were trained for up to 1000 epochs with early stopping, targeting a 44.1kHz sample rate.
</p>

<h4>Validation Method</h4>
<p>
Validation was done by resynthesizing a hold-out portion of the dataset using both <code>TexStat</code> and MSS-trained models. We computed:
<ul>
  <li>FAD metrics with VGGish and <code>TexStat</code>-based embeddings</li>
  <li>Frame-by-frame <code>TexStat</code> and MSS losses (mean ± std)</li>
</ul>
</p>

<div style="overflow-x: auto; max-width: 80%; margin: 0 auto; padding: 10px; box-sizing: border-box;">
<table style="width: 100%; border-collapse: collapse; font-size: 0.9em;">
  <thead style="background-color: #f2f2f2;">
    <tr>
      <th style="border: 1px solid #ccc; padding: 8px;">Texture</th>
      <th style="border: 1px solid #ccc; padding: 8px;">FAD (VGGish)</th>
      <th style="border: 1px solid #ccc; padding: 8px;">FAD (Ours)</th>
      <th style="border: 1px solid #ccc; padding: 8px;"><code>TexStat</code></th>
      <th style="border: 1px solid #ccc; padding: 8px;">MSS</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Bubbles</td><td>35.2</td><td>63.7</td><td>1.2 ± 0.3</td><td>7.9 ± 0.7</td></tr>
    <tr><td>Fire<sup>(1)</sup></td><td>12.1</td><td>570.2</td><td>2.9 ± 2.0</td><td>10.1 ± 1.2</td></tr>
    <tr><td>Keyboard</td><td>13.0</td><td>1945.7</td><td>5.7 ± 2.0</td><td>9.1 ± 0.7</td></tr>
    <tr><td>Rain<sup>(2)</sup></td><td>11.7</td><td>36.6</td><td>0.5 ± 0.2</td><td>9.5 ± 0.3</td></tr>
    <tr><td>River<sup>(2)</sup></td><td>52.7</td><td>38.1</td><td>0.5 ± 0.1</td><td>7.7 ± 0.8</td></tr>
    <tr><td>Shards</td><td>4.6</td><td>8.1</td><td>1.0 ± 0.2</td><td>7.9 ± 0.2</td></tr>
    <tr><td>Waterfall<sup>(1)</sup></td><td>18.2</td><td>28.4</td><td>0.3 ± 0.0</td><td>5.0 ± 0.0</td></tr>
    <tr><td>Wind<sup>(1)</sup></td><td>9.7</td><td>244.7</td><td>0.8 ± 0.5</td><td>5.6 ± 0.1</td></tr>
  </tbody>
</table>

<p style="text-align: center; font-size: 0.85em; color: #666;">
(1) Energy bands were imposed after resynthesis. (2) A loudness tracker was added post-resynthesis. For more comparisons, refer to NoiseBandNet <a href="#ref-noisebandnets">[ref]</a> and our webpage.</p>

</div>

<h4>Discussion</h4>
<p>
These results highlight three main takeaways:
<ol>
  <li>Performance varied across textures, in line with findings by McDermott & Simoncelli and discussed in Subsection <code>Capabilities and Limitations</code>.</li>
  <li>Though our models performed adequately, reconstruction-focused models like NoiseBandNets scored higher—an expected trade-off since we focus on capturing higher-level structure, not perfect reconstruction.</li>
  <li>Our feature-derived metrics often aligned better with perceptual quality, although a proper subjective evaluation was beyond this paper's scope.</li>
</ol>
</p>

</details>

<!-- ---------------------------------------------------------------------------------------------------------------------------------------- -->
<div style="margin-top: 20px;"></div>
<details>
<summary><span style="font-weight: normal; font-size: 1.5em; color: black">3.6. TexDSP Timbre Transfer 🎧</span></summary>

<p>
One known application of DDSP is <strong>timbre transfer</strong> <a href="#ref-engel2020">[Engel et al., 2020]</a>, where pitch and loudness from one source (e.g., voice) drive a model trained on another timbre (e.g., violin), producing violin-like results. This works due to DDSP’s strong inductive bias.
</p>
<p>
In our models, similar effects are observed with textures. For example, a fire sound passed through a water-trained model yields water-like synthesis. But since pitch and loudness are less central in textures, transfer is less clear-cut. Spectral centroid and rate are not as distinctive as pitch in musical sounds. Nonetheless, examples of this phenomenon are available on our webpage.
</p>

[see more](https://cordutie.github.io/tex_framework/timbre_transfer.html)

</details>
