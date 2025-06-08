---
title: Défis Flair
---
<div style="display: flex; justify-content: space-between; font-size: 11pt;">
  <a href="./flair_1_fr.html"><b>🇫🇷 Version française</b></a>
  <a href="../index.html"><b>🔙 Back to FLAIR</b></a>
</div>
<p align="center"><img src="../img/flair_bandeau.jpg" alt="" style="width:100%;max-width:1200px;" /></p>
<br><br>

## FLAIR #2 : textural and temporal information for semantic segmentation from multi-source optical imagery 🌍🌱🏠🌳➡️🛩️🛰️
 
Challenge organized by IGN with the support of the <a href="https://cnes.fr/en" target="_blank"><b>CNES</b></a> and <a href="https://www.connectbycnes.fr/en" target="_blank"><b>Connect by CNES</b></a> with the Copernicus / FPCUP projetc.<br>
<img style="width:100%;max-width:800px;" src="../img/flair-2_logos-hd.png" alt="Drawing"/>
<br/><br/><br/>


>FLAIR #2 <b>datapaper  &#128209;</b>  : https://arxiv.org/pdf/2305.14467.pdf <br/>
>FLAIR #2 <b>NeurIPS datapaper  &#128209;</b>  : https://proceedings.neurips.cc/paper_files/paper/2023/file/353ca88f722cdd0c481b999428ae113a-Paper-Datasets_and_Benchmarks.pdf <br/>
>FLAIR #2 <b>NeurIPS poster  &#128209;</b>  : https://neurips.cc/media/PosterPDFs/NeurIPS%202023/73621.png?t=1699528363.252194 <br/>
>FLAIR #2 <b>repository &#128193;</b> : https://github.com/IGNF/FLAIR-2 <br/>
>FLAIR #2 <b>challenge page &#128187;</b> : https://codalab.lisn.upsaclay.fr/competitions/13447 [closed]

><b>Pre-trained models &#9889;</b> : for now upon request ! 

<br/><br/>


<details><summary><font size=3.5>▶️ Context of the challenge</font><em> (click to expand)</em></summary> 

With this new challenge, participants will be tasked with developing innovative solutions that can effectively harness the textural information from single date aerial imagery and temporal/spectral information from Sentinel-2 satellite time series to enhance semantic segmentation, domain adaptation, and transfer learning. Your solutions should address the challenges of reconciling differing acquisition times, spatial resolutions, accommodating varying conditions, and handling the heterogeneity of semantic classes across different locations.


<br/><br/>
<p align="center"><img src="../img/flair_2_frise.png" alt="" style="width:100%;max-width:1000px;"/></p><br>

</details>
<br>

<details><summary><font size=3.5>▶️ Dataset description</font> <em> (click to expand)</em></summary> 

The FLAIR #2 dataset encompasses 20,384,841,728 annotated pixels at a spatial resolution of 0.20 m from aerial imagery, divided into 77,762 patches of size 512x512. The FLAIR #2 dataset also includes an extensive collection of satellite data, with a total of 51,244 acquisitions of Copernicus Sentinel-2 satellite images. For each area, a comprehensive one-year record of acquisitions has been gathered offering valuable insights into the spatio-temporal dynamics and spectral characteristics of the land cover. Due to the significant difference in spatial resolution between aerial imagery and satellite data, the areas initially defined lack sufficient context as they consist of only a few Sentinel-2 pixels. To address this, a buffer was applied to create larger areas known as super-areas. This ensures that each patch of the dataset is associated with a sufficiently sized super-patch of Sentinel-2 data, providing a minimum level of context from the satellite.<br><br/>

<p align="center"><img src="../img/flair_2_spatial.png" alt="" style="width:100%;max-width:400px;"/></p><br>





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

<br><br>
</details>
<br>

<details><summary><font size=3.5>▶️ Baseline model: U-T&T</font> <em> (click to expand)</em></summary> 

We propose the U-T&T model, a two-branch architecture that combines spatial and temporal information from very high-resolution aerial images and high-resolution satellite images into a single output. The U-Net architecture is employed for the spatial/texture branch, using a ResNet34 backbone model pre-trained on ImageNet. For the spatio-temporal branch, the U-TAE architecture incorporates a Temporal self-Attention Encoder (TAE) to explore the spatial and temporal characteristics of the Sentinel-2 time series data, applying attention masks at different resolutions during decoding. This model allows for the fusion of learned information from both sources, enhancing the representation of mono-date and time series data.
<br><br>
</details>
<br>

<details><summary><font size=3.5>▶️ Download the dataset</font> <em>(click to expand)</em></summary> 

<br><br>
<center>
<table style="width:80%;max-width:700px;">
  <tr>
    <th>Data</th><th>Size</th><th>Type</th><th>Link</th>
 </tr>
 <tr><td colspan="4" height = 10px></td>
 </tr>
  <tr>
    <td>Aerial images - train</td><td>50.7 Go</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_aerial_train.zip"><b>download</b></a>
  </tr>
   <tr>
    <td>Aerial images - test</td><td>13.4 Go</td><td>.zip</td>
     <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_aerial_test.zip"><b>download</b></a>  
  </tr>
 </tr>
  <tr>
    <td>Sentinel-2 images - train</td><td>22.8 Go</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_sen_train.zip"><b>download</b></a>
  </tr>
   <tr>
    <td>Sentinel-2 images - test</td><td>6 Go</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_sen_test.zip"><b>download</b></a>
  </tr>
  <tr>
    <td>Labels - train</td><td>485 Mo</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_labels_train.zip"><b>download</b></a>
  </tr>
  <tr style="cellspacing: 10px">
    <td>Labels - test</td><td>108 Mo</td><td>.zip</td>
     <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_labels_test.zip"><b>download</b></a>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Aerial metadata</td><td>16.1 Mo</td><td>.json</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_aerial_metadata.zip"><b>download</b></a>
  </tr>
  <tr>
    <td>Aerial <-> Sentinel-2 matching dict</td><td>16.1 Mo</td><td>.json</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_centroids_sp_to_patch.zip"><b>download</b></a>
  </tr>
  <tr>
    <td>Satellite shapes</td><td>392 Ko</td><td>.gpkg</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_satellite_shapes.zip"><b>download</b></a>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Toy dataset (subset of train and test)</td><td>1.6 Go</td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_toy_dataset.zip"><b>download</b></a></td>
  </tr>
</table>
</center><br><br>
Alternatively, get the dataset from our <a style="font-size: 10pt" href="https://huggingface.co/datasets/IGNF/FLAIR"><b>HuggingFace Page</b></a>.
<br/><br/>

</details>
<br><br>


### Reference

Please include a citation to the following paper if you use the FLAIR #2 dataset: 

Plain text:
```
Anatol Garioud, Nicolas Gonthier, Loic Landrieu, Apolline De Wit, Marion Valette, Marc Poupée, Sébastien Giordano and Boris Wattrelos. 2023. 
FLAIR: a Country-Scale Land Cover Semantic Segmentation Dataset From Multi-Source Optical Imagery. (2023).
In proceedings of Advances in Neural Information Processing Systems (NeurIPS) 2023.
DOI: https://doi.org/10.48550/arXiv.2310.13336
```

BibTex:
```
@inproceedings{ign2023flair2,
      title={FLAIR: a Country-Scale Land Cover Semantic Segmentation Dataset From Multi-Source Optical Imagery}, 
      author={Anatol Garioud and Nicolas Gonthier and Loic Landrieu and Apolline De Wit and Marion Valette and Marc Poupée and Sébastien Giordano and Boris Wattrelos},
      year={2023},
      booktitle={Advances in Neural Information Processing Systems (NeurIPS) 2023},
      doi={https://doi.org/10.48550/arXiv.2310.13336},
}
```
