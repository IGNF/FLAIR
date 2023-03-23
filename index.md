---
title: FLAIR Challenges
---

# Welcome to IGN's FLAIR datasets page!
<p align="center"><img src="img/flair_logo.jpg" alt="" width="40%" /></p>


<a style="font-size: 11pt" href="./index_fr.html"><b>French version</b></a>
<br>

The French National Institute of Geographical and Forest Information (IGN) presents its AI challenges and benchmark datasets FLAIR (for French Land cover from Aerospace ImageRy). 
[Learn more about the context of these challenges.](./why_flair.html) 

<hr><p align="center"><img src="img/visuel_FLAIR_bandeau.jpg" alt="" width="100%" /></p>
<hr>
You can reach us at : <a href = "mailto:ai-challenge@ign.fr?subject=FLAIR - AI challenge @IGN">ai-challenge@ign.fr</a>
<br><br>


## FLAIR #1 : semantic segmentation and domain adaptation

<img src="img/logo_ign_sfpt.png" alt="" width="30%" />

The challenge took place on Codalab from November, 21st 2022 to March, 21st 2023. See the results <a style="font-size: 10pt" href="https://codalab.lisn.upsaclay.fr/competitions/8769"><b>here.</b></a><br/>

FLAIR #1 <b>datapaper  &#128209;</b>  : https://arxiv.org/pdf/2211.12979.pdf <br>
FLAIR #1 <b>repository &#128193;</b> : https://github.com/IGNF/FLAIR-1-AI-Challenge<br>

### Description

We present here a large dataset ( >20 billion pixels) of aerial imagery, topographic information and land cover (buildings, water, forest, agriculture...) annotations with the aim to further advance research on semantic segmentation , domain adaptation and transfer learning. Countrywide remote sensing aerial imagery is by necessity acquired at different times and dates and under different conditions. Likewise, at large scales, the characteristics of semantic classes can vary depending on location and become heterogenous. This opens up challenges for the spatial and temporal generalization of deep learning models! 

The FLAIR-one dataset consists of 77,412 high resolution (0.2 m spatial resolution) patches with 19 semantic classes. For this challenge and the associated baselines, due to imbalanced class frequencies, the number of classes has been reduced to 13 (remapping >12 to 13, see the datapaper for explanation). 
<br>

<center>
<table style="width:50%">
<thead>
  <tr><th width=20%></th><th>Class</th><th width=15%>Value</th></tr>
</thead>
<tbody>
  <tr><td bgcolor='#db0e9a'></td><td>building</td><td>1</td></tr>
  <tr><td bgcolor='#938e7b'></td><td>pervious surface</td><td>2</td></tr>
  <tr><td bgcolor='#f80c00'></td><td>impervious surface</td><td>3</td></tr>
  <tr><td bgcolor='#a97101'></td><td>bare soil</td><td>4</td></tr>
  <tr><td bgcolor='#1553ae'></td><td>water</td><td>5</td></tr>
  <tr><td bgcolor='#194a26'></td><td>coniferous</td><td>6</td></tr>
  <tr><td bgcolor='#46e483'></td><td>deciduous</td><td>7</td></tr>
  <tr><td bgcolor='#f3a60d'></td><td>brushwood</td><td>8</td></tr>
  <tr><td bgcolor='#660082'></td><td>vineyard</td><td>9</td></tr>
  <tr><td bgcolor='#55ff00'></td><td>herbaceous vegetation</td><td>10</td></tr>
  <tr><td bgcolor='#fff30d'></td><td>agricultural land</td><td>11</td></tr>
  <tr><td bgcolor='#e4df7c'></td><td>plowed land</td><td>12</td></tr>
  <tr><td bgcolor='#3de6eb'></td><td>swimming_pool</td><td>13</td></tr>
  <tr><td bgcolor='#ffffff'></td><td>snow</td><td>14</td></tr>
  <tr><td bgcolor='#8ab3a0'></td><td>clear cut</td><td>15</td></tr>
  <tr><td bgcolor='#6b714f'></td><td>mixed</td><td>16</td></tr>
  <tr><td bgcolor='#c5dc42'></td><td>ligneous</td><td>17</td></tr>
  <tr><td bgcolor='#9999ff'></td><td>greenhouse</td><td>18</td></tr>
  <tr><td bgcolor='#000000'></td><td>other</td><td>19</td></tr>
</tbody>
</table>
</center>


The dataset covers a total of approximatly 800 km², with patches that have been sampled accross the entire metropolitan French territory to be illustrating the different climate and landscapes (spatial domains). The aerial images included in the dataset were acquired during different months and years (temporal domains).


<table>
    <tr>
        <td style="text-align: center"><img src="img/ortho.png" 
            alt="Aerial image ORHTO HR" title="Michael Jordan" /></td>
        <td style="text-align: center"><img src="img/labels.png" alt="James Worthy" 
            title="Labels" /></td>
    </tr>
    <tr>
        <td style="text-align: center">Aerial image ORHTO HR&#174;</td>
        <td style="text-align: center">Labels</td>
    </tr>
</table>


The test dataset consists of 15,700 patches from 10 domains not included in the train dataset. Class frequency and temporal domains of the test dataset includes a shift from the train dataset allowing to assess the domain adaptation capabilities of developped approaches.


### Baseline model

A U-Net architecture with a pre-trained ResNet34 encoder from the pytorch segmentation models library has been used for the baselines. The used architecture allows integration of patch-wise metadata information and employs commonly used image data augmentation techniques. Codes are available in the FLAIR #1 repository.


### Datasets

<table>
  <tr>
    <th>Data</th>
    <th>Size</th>
    <th>Type</th>
    <th>Link</th>
 </tr>
 <tr><td colspan="4" height = 10px></td>
 </tr>
  <tr>
    <td>Aerial images - train</td>
    <td>50.7 Go</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
   <tr>
    <td>Aerial images - test</td>
    <td>13.4 Go</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr>
    <td>Labels - train</td>
    <td>485 Mo</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr style="cellspacing: 10px">
    <td>Labels - test</td>
    <td>124 Mo</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Aerial metadata</td>
    <td>16.1 Mo</td>
    <td>.json</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr>
    <td>Areas shapes</td>
    <td>392 Ko</td>
    <td>.gpkg</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr>
    <td>Toy dataset (train and test)</td>
    <td>215 Mo</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
</table>

### Reference

Please include a citation to the following paper if you use the FLAIR #1 dataset: 

```
@article{garioud2022flair1,
  doi = {10.13140/RG.2.2.30183.73128/1},
  url = {https://arxiv.org/pdf/2211.12979.pdf},
  author = {Garioud, Anatol and Peillet, Stéphane and Bookjans, Eva and Giordano, Sébastien and Wattrelos, Boris},
  title = {FLAIR #1: semantic segmentation and domain adaptation dataset},
  publisher = {arXiv},
  year = {2022}
}
```

<br><br>

## FLAIR #2 : texture and time from multimodal optical imagery for segmentic segmentation 

<img src="img/logo_ign_cnes.png" alt="" width="30%" />

<b>Coming soon !</b> 

<!---
FLAIR #2 repository : https://github.com/IGNF/FLAIR-2-AI-Challenge
-->
