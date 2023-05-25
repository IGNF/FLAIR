---
title: FLAIR Challenges
---
<a style="font-size: 9.5pt" href="./index_fr.html"><b>Version française</b></a>

# Welcome to IGN's FLAIR datasets page!

<p align="center"><img src="img/flair_bandeau.jpg" alt="" style="width:100%;max-width:1200px;" /></p>
<!---
[Learn more about the context of these challenges.](./why_flair.html)<br>
--->
<center>
<table style="width:100%;max-width:1400px;">
<tr>
<td width=40% style="text-align: center; padding: 40px">The French National Institute of Geographical and Forest Information (IGN) presents its AI challenges and benchmark datasets FLAIR (for French Land cover from Aerospace ImageRy). The FLAIR datasets include Earth Observation data from different aerospace sensors. These datasets cover large scales and reflect real world cases of land cover mapping tasks. <br><br>
  
<div style="padding: 5px; border: 1px solid red; margin-bottom: 8px;">  
<code style="padding: 2px 4px; font-size: 100%; color: #c7254e;  border-radius: 0;">Explore the datasets and baseline codes ! </code><br/><br/>
<ul style="list-style-type:none;">
<li> <a style="font-size: 11.5pt" href="#FLAIR1">FLAIR #1 challenge: aerial imagery</a></li>
<li> <a style="font-size: 11.5pt" href="#FLAIR2">FLAIR #2 challenge: multimodal optical dataset</a></li>
</ul>
</div>
  
<br>
We are committed to supporting research and fostering innovation in the fields of Earth Observation. For any question concerning the data, their access and exploitation, as well as for any idea of future datasets or suggestion of topics, simply contact us at the address:<br/> <a href = "mailto:ai-challenge@ign.fr?subject=FLAIR - AI challenge @IGN">ai-challenge@ign.fr</a> 
<br><br>
<img style="width:40%;max-width:400px;" class="center-block" src="img/ETALAB_LICENCE_FLAIR.png"><br><br>The FLAIR datasets are under the <a href="https://www.etalab.gouv.fr/wp-content/uploads/2018/11/open-licence.pdf" target="_blank"><b>Open Licence 2.0</b></a> of Etalab. Remember to cite the associated datapaper to each dataset.
</td>

<td width=60% style="text-align: center"><img src="img/FLAIR_recap_3.png" alt="" style="width:100%;max-width:1000px;" /></td>
</tr>
</table>
</center>

<hr>

<br><br/><br/><a id="FLAIR1"></a><br/><br/><br/><br/><br/><br/>



## FLAIR #1 : semantic segmentation and domain adaptation 🌍🌱🏠🌳➡️🛩️

Challenge organized by IGN with the support of the <a href="https://www.sfpt.fr/" target="_blank"><b>SFPT.</b></a><br>
The challenge took place on Codalab from November, 21st 2022 to March, 21st 2023. See the results <a href="https://codalab.lisn.upsaclay.fr/competitions/8769" target="_blank"><b>here.</b></a><br/><br/><br/>

>FLAIR #1 <b>datapaper  &#128209;</b>  : https://arxiv.org/pdf/2211.12979.pdf <br/>
>FLAIR #1 <b>repository &#128193;</b> : https://github.com/IGNF/FLAIR-1-AI-Challenge

<br/><br/>
<p align="center"><img src="img/flair_dataset_illustration_dark-min.png" alt="" style="width:65%;max-width:600px;"/></p><br>

### Description

We present here a large dataset ( >20 billion pixels) of aerial imagery, topographic information and land cover (buildings, water, forest, agriculture...) annotations with the aim to further advance research on semantic segmentation , domain adaptation and transfer learning. Countrywide remote sensing aerial imagery is by necessity acquired at different times and dates and under different conditions. Likewise, at large scales, the characteristics of semantic classes can vary depending on location and become heterogenous. This opens up challenges for the spatial and temporal generalization of deep learning models! 

The FLAIR-one dataset consists of 77,412 high resolution patches (512x512 at 0.2 m spatial resolution) with 19 semantic classes. For this challenge and the associated baselines, due to imbalanced class frequencies, the number of classes has been reduced to 13 (remapping >12 to 13, see the datapaper for explanation).<br/>

<center>
<table style="width:80%;max-width:700px;">
<thead>
  <tr><th width=7%></th><th>Class</th><th style='text-align: center' width=15%>Value</th><th style='text-align: center'>Freq.-train (%)</th><th style='text-align: center'>Freq.-test (%)</th></tr>
</thead>
<tbody>
  <tr><td bgcolor='#db0e9a'></td><td>building</td><td style='text-align: center'>1</td><td style='text-align: center'>8.14</td><td style='text-align: center'>8.6</td></tr>
  
  <tr><td bgcolor='#938e7b'></td><td>pervious surface</td><td style='text-align: center'>2</td><td style='text-align: center'>8.25</td><td style='text-align: center'>7.34</td></tr>
  
  <tr><td bgcolor='#f80c00'></td><td>impervious surface</td><td style='text-align: center'>3</td><td style='text-align: center'>13.72</td><td style='text-align: center'>14.98</td></tr>
  
  <tr><td bgcolor='#a97101'></td><td>bare soil</td><td style='text-align: center'>4</td><td style='text-align: center'>3.47</td><td style='text-align: center'>4.36</td></tr>
  
  <tr><td bgcolor='#1553ae'></td><td>water</td><td style='text-align: center'>5</td><td style='text-align: center'>4.88</td><td style='text-align: center'>5.98</td></tr>
  
  <tr><td bgcolor='#194a26'></td><td>coniferous</td><td style='text-align: center'>6</td><td style='text-align: center'>2.74</td><td style='text-align: center'>2.39</td></tr>
  
  <tr><td bgcolor='#46e483'></td><td>deciduous</td><td style='text-align: center'>7</td><td style='text-align: center'>15.38</td><td style='text-align: center'>13.91</td></tr>
  
  <tr><td bgcolor='#f3a60d'></td><td>brushwood</td><td style='text-align: center'>8</td><td style='text-align: center'>6.95</td><td style='text-align: center'>6.91</td></tr>
  
  <tr><td bgcolor='#660082'></td><td>vineyard</td><td style='text-align: center'>9</td><td style='text-align: center'>3.13</td><td style='text-align: center'>3.87</td></tr>
  
  <tr><td bgcolor='#55ff00'></td><td>herbaceous vegetation</td><td style='text-align: center'>10</td><td style='text-align: center'>17.84</td><td style='text-align: center'>22.17</td></tr>
  
  <tr><td bgcolor='#fff30d'></td><td>agricultural land</td><td style='text-align: center'>11</td><td style='text-align: center'>10.98</td><td style='text-align: center'>6.95</td></tr>
  
  <tr><td bgcolor='#e4df7c'></td><td>plowed land</td><td style='text-align: center'>12</td><td style='text-align: center'>3.88</td><td style='text-align: center'>2.25</td></tr>
  
  <tr><td bgcolor='#3de6eb'></td><td>swimming pool</td><td style='text-align: center'>13</td><td style='text-align: center'>0.03</td><td style='text-align: center'>0.04</td></tr>
  
  <tr><td bgcolor='#ffffff'></td><td>snow</td><td style='text-align: center'>14</td><td style='text-align: center'>0.15</td><td style='text-align: center'>-</td></tr>
  
  <tr><td bgcolor='#8ab3a0'></td><td>clear cut</td><td style='text-align: center'>15</td><td style='text-align: center'>0.15</td><td style='text-align: center'>0.01</td></tr>
  
  <tr><td bgcolor='#6b714f'></td><td>mixed</td><td style='text-align: center'>16</td><td style='text-align: center'>0.05</td><td style='text-align: center'>-</td></tr>
  
  <tr><td bgcolor='#c5dc42'></td><td>ligneous</td><td style='text-align: center'>17</td><td style='text-align: center'>0.01</td><td style='text-align: center'>0.03</td></tr>
  
  <tr><td bgcolor='#9999ff'></td><td>greenhouse</td><td style='text-align: center'>18</td><td style='text-align: center'>0.12</td><td style='text-align: center'>0.2</td></tr>
  
  <tr><td bgcolor='#000000'></td><td>other</td><td style='text-align: center'>19</td><td style='text-align: center'>0.14</td><td style='text-align: center'>-</td></tr>
</tbody>
</table>
</center>


The dataset covers a total of approximatly 812 km², with patches that have been sampled accross the entire metropolitan French territory to be illustrating the different climate and landscapes (spatial domains). The aerial images included in the dataset were acquired during different months and years (temporal domains).


<table>
    <tr>
        <td style="text-align: center"><img src="img/flair_ortho.png" 
            alt="Aerial image ORTHO HR" title="ORHTO HR" /></td>
        <td style="text-align: center"><img src="img/flair_labels.png" alt="Labels" 
            title="Labels" /></td>
    </tr>
    <tr>
        <td style="text-align: center">Aerial image ORHTO HR&#174;</td>
        <td style="text-align: center">Labels</td>
    </tr>
</table>


The test dataset consists of 15,700 patches from 10 domains not included in the train dataset. Class frequency and temporal domains of the test dataset includes a shift from the train dataset allowing to assess the domain adaptation capabilities of developped approaches.
<br/><br/>

### Baseline model

A U-Net architecture with a pre-trained ResNet34 encoder from the pytorch segmentation models library has been used for the baselines. The used architecture allows integration of patch-wise metadata information and employs commonly used image data augmentation techniques. Codes are available in the FLAIR #1 repository.
<br/><br/>

<p align="center"><img src="img/flair_predict.gif" alt="" style="width:65%;max-width:900px;" /></p>
<br/><br/>

### Datasets

<center>
<table style="width:80%;max-width:700px;">
  <tr>
    <th>Data</th><th>Size</th><th>Type</th><th>Link</th>
 </tr>
 <tr><td colspan="4" height = 10px></td>
 </tr>
  <tr>
    <td>Aerial images - train</td><td>50.7 Go</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_1/flair_aerial_train.zip"><b>download</b></a>
  </tr>
   <tr>
    <td>Aerial images - test</td><td>13.4 Go</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_1/flair_1_aerial_test.zip"><b>download</b></a>
  </tr>
  <tr>
    <td>Labels - train</td><td>485 Mo</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_1/flair_labels_train.zip"><b>download</b></a>
  </tr>
  <tr style="cellspacing: 10px">
    <td>Labels - test</td><td>124 Mo</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_1/flair_1_labels_test.zip"><b>download</b></a>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Aerial metadata</td><td>16.1 Mo</td><td>.json</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_1/flair-1_metadata_aerial.zip"><b>download</b></a>
  </tr>
  <tr>
    <td>Areas shapes</td><td>392 Ko</td><td>.gpkg</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_1/flair_1_shapes.gpkg"><b>download</b></a>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Toy dataset (subset of train and test)</td><td>215 Mo</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_1/flair_1_toy_dataset.zip"><b>download</b></a>
  </tr>
</table>
</center>
<br/><br/>

### Reference

Please include a citation to the following paper if you use the FLAIR #1 dataset: 

Plain text:
```
Anatol Garioud, Stéphane Peillet, Eva Bookjans, Sébastien Giordano, and Boris Wattrelos. 2022. 
FLAIR #1: semantic segmentation and domain adaptation dataset. (2022). 
DOI:https://doi.org/10.13140/RG.2.2.30183.73128/1
```

BibTex:
```
@article{ign2022flair1,
  doi = {10.13140/RG.2.2.30183.73128/1},
  url = {https://arxiv.org/pdf/2211.12979.pdf},
  author = {Garioud, Anatol and Peillet, Stéphane and Bookjans, Eva and Giordano, Sébastien and Wattrelos, Boris},
  title = {FLAIR #1: semantic segmentation and domain adaptation dataset},
  publisher = {arXiv},
  year = {2022}
}
```


















<br><br/><br/><a id="FLAIR2"></a><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>


## FLAIR #2 : textural and temporal information for semantic segmentation from multi-source optical imagery 🌍🌱🏠🌳➡️🛩️🛰️
 
Challenge organized by IGN with the support of the <a href="https://cnes.fr/en" target="_blank"><b>CNES</b></a> and <a href="https://www.connectbycnes.fr/en" target="_blank"><b>Connect by CNES</b></a> with the Copernicus / FPCUP projetc.<br>
<img style="width:100%;max-width:1000px;" src="https://drive.google.com/uc?export=view&amp;id=1AsEPakQwUrBKreV3qOPQq9SjUfRRJkIc" alt="Drawing"/>
<br/><br/><br/>


>FLAIR #2 <b>datapaper  &#128209;</b>  : https://arxiv.org/pdf/2305.14467.pdf <br/>
>FLAIR #2 <b>repository &#128193;</b> : https://github.com/IGNF/FLAIR-2-AI-Challenge


<br/><br/>

### Context

With this new challenge, participants will be tasked with developing innovative solutions that can effectively harness the textural information from single date aerial imagery and temporal/spectral information from Sentinel-2 satellite time series to enhance semantic segmentation, domain adaptation, and transfer learning. Your solutions should address the challenges of reconciling differing acquisition times, spatial resolutions, accommodating varying conditions, and handling the heterogeneity of semantic classes across different locations.


<br/><br/>
<p align="center"><img src="img/flair_2_frise.png" alt="" style="width:80%;max-width:1200px;"/></p><br>



### Dataset

The FLAIR #2 dataset encompasses 20,384,841,728 annotated pixels at a spatial resolution of 0.20 m from aerial imagery, divided into 77,762 patches of size 512x512. The FLAIR #2 dataset also includes an extensive collection of satellite data, with a total of 51,244 acquisitions of Copernicus Sentinel-2 satellite images. For each area, a comprehensive one-year record of acquisitions has been gathered offering valuable insights into the spatio-temporal dynamics and spectral characteristics of the land cover. Due to the significant difference in spatial resolution between aerial imagery and satellite data, the areas initially defined lack sufficient context as they consist of only a few Sentinel-2 pixels. To address this, a buffer was applied to create larger areas known as super-areas. This ensures that each patch of the dataset is associated with a sufficiently sized super-patch of Sentinel-2 data, providing a minimum level of context from the satellite.<br><br/>

<p align="center"><img src="img/flair_2_spatial.png" alt="" style="width:100%;max-width:400px;"/></p><br>





The dataset covers 50 spatial domains, encompassing 916 areas spanning 817 km². With 13 semantic classes (plus 6 not used in this challenge), this dataset provides a robust foundation for advancing land cover mapping techniques.<br><br>

<center>
<table style="width:80%;max-width:700px;">
<thead>
  <tr><th width=7%></th><th>Class</th><th style='text-align: center' width=15%>Value</th><th style='text-align: center'>Freq.-train (%)</th><th style='text-align: center'>Freq.-test (%)</th></tr>
</thead>
<tbody>
  <tr><td bgcolor='#db0e9a'></td><td>building</td><td style='text-align: center'>1</td><td style='text-align: center'>8.14</td><td style='text-align: center'>3.26</td></tr>
  
  <tr><td bgcolor='#938e7b'></td><td>pervious surface</td><td style='text-align: center'>2</td><td style='text-align: center'>8.25</td><td style='text-align: center'>3.82</td></tr>
  
  <tr><td bgcolor='#f80c00'></td><td>impervious surface</td><td style='text-align: center'>3</td><td style='text-align: center'>13.72</td><td style='text-align: center'>5.87</td></tr>
  
  <tr><td bgcolor='#a97101'></td><td>bare soil</td><td style='text-align: center'>4</td><td style='text-align: center'>3.47</td><td style='text-align: center'>1.6</td></tr>
  
  <tr><td bgcolor='#1553ae'></td><td>water</td><td style='text-align: center'>5</td><td style='text-align: center'>4.88</td><td style='text-align: center'>3.17</td></tr>
  
  <tr><td bgcolor='#194a26'></td><td>coniferous</td><td style='text-align: center'>6</td><td style='text-align: center'>2.74</td><td style='text-align: center'>10.24</td></tr>
  
  <tr><td bgcolor='#46e483'></td><td>deciduous</td><td style='text-align: center'>7</td><td style='text-align: center'>15.38</td><td style='text-align: center'>24.79</td></tr>
  
  <tr><td bgcolor='#f3a60d'></td><td>brushwood</td><td style='text-align: center'>8</td><td style='text-align: center'>6.95</td><td style='text-align: center'>3.81</td></tr>
  
  <tr><td bgcolor='#660082'></td><td>vineyard</td><td style='text-align: center'>9</td><td style='text-align: center'>3.13</td><td style='text-align: center'>2.55</td></tr>
  
  <tr><td bgcolor='#55ff00'></td><td>herbaceous vegetation</td><td style='text-align: center'>10</td><td style='text-align: center'>17.84</td><td style='text-align: center'>19.76</td></tr>
  
  <tr><td bgcolor='#fff30d'></td><td>agricultural land</td><td style='text-align: center'>11</td><td style='text-align: center'>10.98</td><td style='text-align: center'>18.19</td></tr>
  
  <tr><td bgcolor='#e4df7c'></td><td>plowed land</td><td style='text-align: center'>12</td><td style='text-align: center'>3.88</td><td style='text-align: center'>1.81</td></tr>
  
  <tr><td bgcolor='#3de6eb'></td><td>swimming pool</td><td style='text-align: center'>13</td><td style='text-align: center'>0.01</td><td style='text-align: center'>0.02</td></tr>
  
  <tr><td bgcolor='#ffffff'></td><td>snow</td><td style='text-align: center'>14</td><td style='text-align: center'>0.15</td><td style='text-align: center'>-</td></tr>
  
  <tr><td bgcolor='#8ab3a0'></td><td>clear cut</td><td style='text-align: center'>15</td><td style='text-align: center'>0.15</td><td style='text-align: center'>0.82</td></tr>
  
  <tr><td bgcolor='#6b714f'></td><td>mixed</td><td style='text-align: center'>16</td><td style='text-align: center'>0.05</td><td style='text-align: center'>0.12</td></tr>
  
  <tr><td bgcolor='#c5dc42'></td><td>ligneous</td><td style='text-align: center'>17</td><td style='text-align: center'>0.01</td><td style='text-align: center'>-</td></tr>
  
  <tr><td bgcolor='#9999ff'></td><td>greenhouse</td><td style='text-align: center'>18</td><td style='text-align: center'>0.12</td><td style='text-align: center'>0.15</td></tr>
  
  <tr><td bgcolor='#000000'></td><td>other</td><td style='text-align: center'>19</td><td style='text-align: center'>0.14</td><td style='text-align: center'>0.04</td></tr>
</tbody>
</table>
</center>

<br>

### Baseline model

We propose the U-T&T model, a two-branch architecture that combines spatial and temporal information from very high-resolution aerial images and high-resolution satellite images into a single output. The U-Net architecture is employed for the spatial/texture branch, using a ResNet34 backbone model pre-trained on ImageNet. For the spatio-temporal branch, the U-TAE architecture incorporates a Temporal self-Attention Encoder (TAE) to explore the spatial and temporal characteristics of the Sentinel-2 time series data, applying attention masks at different resolutions during decoding. This model allows for the fusion of learned information from both sources, enhancing the representation of mono-date and time series data.


<br><br>


### Dataset

<center>
<table style="width:80%;max-width:700px;">
  <tr>
    <th>Data</th><th>Size</th><th>Type</th><th>Link</th>
 </tr>
 <tr><td colspan="4" height = 10px></td>
 </tr>
  <tr>
    <td>Aerial images - train</td><td>50.7 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
   <tr>
    <td>Aerial images - test</td><td>13.4 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
 </tr>
  <tr>
    <td>Sentinel-2 images - train</td><td>22.8 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
   <tr>
    <td>Sentinel-2 images - test</td><td>6 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Labels - train</td><td>485 Mo</td><td>.zip</td>
    <td>-</td>
  </tr>
  <tr style="cellspacing: 10px">
    <td>Labels - test</td><td>108 Mo</td><td>.zip</td>
    <td>-</td>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Aerial metadata</td><td>16.1 Mo</td><td>.json</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Aerial <-> Sentinel-2 matching dict</td><td>16.1 Mo</td><td>.json</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Areas shapes</td><td>392 Ko</td><td>.gpkg</td>
    <td>-</td>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Toy dataset (subset of train and test)</td><td>1.6 Go</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_toy_dataset.zip"><b>download</b></a></td>
  </tr>
</table>
</center>
<br/><br/>



### Reference

Please include a citation to the following paper if you use the FLAIR #2 dataset: 


Plain text:
```
Anatol Garioud, Apolline De Wit, Marc Poupée, Marion Valette, Sébastien Giordano, and Boris Wattrelos. 2023. 
FLAIR #2: textural and temporal information for semantic segmentation from multi-source optical imagery. (2023). 
DOI:https://doi.org/10.13140/RG.2.2.30938.93128/2
```

BibTex:
```
@article{ign2023flair2,
  doi = {10.13140/RG.2.2.30938.93128/2},
  url = {https://arxiv.org/pdf/2305.14467.pdf},
  author = {Garioud, Anatol and {DE Wit}, Apolline and Poupée, Marc and Valette, Marion and Giordano, Sébastien and Wattrelos, Boris},
  title = {FLAIR #2: textural and temporal information for semantic segmentation from multi-source optical imagery},
  publisher = {arXiv},
  year = {2023}
}
```
