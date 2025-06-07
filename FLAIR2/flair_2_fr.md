---
title: Défis Flair
---
🇬🇧 <a style="font-size: 11pt" href="./flair_2.html"><b>English version</b></a>
🔙 <a style="font-size: 11pt" href="../index.html"><b>Retour FLAIR</b></a>

# Welcome to IGN's FLAIR datasets page!

<p align="center"><img src="../img/flair_bandeau.jpg" alt="" style="width:100%;max-width:1200px;" /></p>


<br>
## FLAIR #2 : Information texturale et temporelle à partir d'imagerie optique multimodal pour la segmentation sémantique 🌍🌱🏠🌳➡️🛩️🛰️
 
Challenge organisé par l'IGN avec le soutient du <a href="https://cnes.fr/en" target="_blank"><b>CNES</b></a> et de <a href="https://www.connectbycnes.fr/" target="_blank"><b>Connect by CNES</b></a> dans le cadre d'un projet Copernicus / FPCUP.<br>
<img style="width:100%;max-width:800px;" src="../img/flair-2_logos-hd.png" alt="Drawing"/>
<br/><br/><br/>

>FLAIR #2 <b>datapaper  &#128209;</b>  : https://arxiv.org/pdf/2305.14467.pdf <br/>
>FLAIR #2 <b>NeurIPS datapaper  &#128209;</b>  : https://proceedings.neurips.cc/paper_files/paper/2023/file/353ca88f722cdd0c481b999428ae113a-Paper-Datasets_and_Benchmarks.pdf <br/>
>FLAIR #2 <b>NeurIPS poster  &#128209;</b>  : https://neurips.cc/media/PosterPDFs/NeurIPS%202023/73621.png?t=1699528363.252194 <br/>
>FLAIR #2 <b>dépôt GitHub &#128193;</b> : https://github.com/IGNF/FLAIR-2 <br/>
>FLAIR #2 <b>page du défi &#128187;</b> : https://codalab.lisn.upsaclay.fr/competitions/13447 [fermé]

><b>Modèles pré-entraînés</b> : pour l'instant sur demande ! 

<br/><br/>


<details><summary><font size=3.5>▶️ Contexte du challenge</font><em> (cliquer pour agrandir)</em></summary> 

Avec ce nouveau défi, les participants auront pour tâche de développer des solutions innovantes qui peuvent exploiter efficacement les informations texturales des images aériennes prises à une seule date, ainsi que les informations temporelles/spectrales provenant des séries temporelles des satellites Sentinel-2, afin d'améliorer la segmentation sémantique, l'adaptation de domaine et l'apprentissage par transfert. Vos solutions devraient relever les défis liés à la conciliation des différentes périodes d'acquisition, des résolutions spatiales différentes, de l'adaptation aux conditions d'acquisitions variables et de la gestion de l'hétérogénéité des classes sémantiques.


<br/><br/>
<p align="center"><img src="../img/flair_2_frise.png" alt="" style="width:100%;max-width:1000px;"/></p><br>

</details>
<br>

<details><summary><font size=3.5>▶️ Description du dataset</font> <em> (cliquer pour agrandir)</em></summary> 

Le jeu de données FLAIR #2 comprend 20,384,841,728 pixels annotés avec une résolution spatiale de 0,20 m à partir d'images aériennes, répartis en 77,762 patchs de taille 512x512. Le jeu de données FLAIR #2 inclut également une vaste collection de données satellites, avec un total de 51,244 acquisitions d'images des satellites Copernicus Sentinel-2. Pour chaque zone, les acquisitions sur un an ont été retenues, offrant des informations précieuses sur la dynamique spatio-temporelle et les caractéristiques spectrales de la couverture terrestre. En raison de la différence significative de résolution spatiale entre les images aériennes et les données satellites, les zones initialement définies manquent de contexte suffisant car elles ne sont composées que de quelques pixels Sentinel-2. Pour remédier à cela, une marge a été appliquée pour créer des zones plus grandes appelées super-zones. Cela garantit que chaque patch du jeu de données est associé à une super-zone de données Sentinel-2 de taille suffisante, offrant un niveau minimum de contexte provenant du satellite.<br><br/>

<p align="center"><img src="../img/flair_2_spatial.png" alt="" style="width:100%;max-width:400px;"/></p><br>

Le jeu de données couvre 50 domaines spatial, comprenant 916 zones réparties sur 817 km². Avec 13 classes sémantiques (plus 6 non utilisées dans ce défi), ce jeu de données constitue une base solide pour faire progresser les techniques de cartographie de la couverture du sol.<br><br>

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

<details><summary><font size=3.5>▶️ Modèle de référence (baseline): U-T&T</font> <em> (cliquer pour agrandir)</em></summary> 

Nous proposons le modèle U-T&T, une architecture à deux branches qui combine les informations spatiales et temporelles à partir d'images aériennes très haute résolution et d'images satellites haute résolution en une seule sortie. L'architecture U-Net est utilisée pour la branche spatiale/texture, en utilisant un modèle avec un encodeur ResNet34 pré-entraîné sur ImageNet. Pour la branche spatio-temporelle, l'architecture U-TAE intègre un Encodeur à Attention Temporelle (TAE) pour explorer les caractéristiques spatiales et temporelles des séries temporelles de Sentinel-2, en appliquant des masques d'attention à différentes résolutions lors du décodage. Ce modèle permet la fusion des informations apprises à partir des deux sources.
<br><br>
</details>
<br>

<details><summary><font size=3.5>▶️ Téléchargement du dataset</font> <em>(cliquer pour agrandir)</em></summary> 

Pour l'instant sur inscription au défi ! <br>

<center>
<table style="width:80%;max-width:700px;">
  <tr>
    <th>Données</th><th>Volume</th><th>Type</th><th>Lien</th>
 </tr>
 <tr><td colspan="4" height = 10px></td>
 </tr>
  <tr>
    <td>Images aériennes - entraînement</td><td>50.7 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
   <tr>
    <td>Images aériennes - test</td><td>13.4 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
 </tr>
  <tr>
    <td>Images Sentinel-2 - entraînement</td><td>22.8 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
   <tr>
    <td>Images Sentinel-2 - test</td><td>6 Go</td><td>.zip</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Annotations - entraînement</td><td>485 Mo</td><td>.zip</td>
    <td>-</td>
  </tr>
  <tr style="cellspacing: 10px">
    <td>Annotations - test</td><td>108 Mo</td><td>.zip</td>
    <td>-</td>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Métadonnées aériennes</td><td>16.1 Mo</td><td>.json</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Correspondance images aériennes <-> Sentinel-2</td><td>16.1 Mo</td><td>.json</td>
    <td>-</td>
  </tr>
  <tr>
    <td>Shapefile zones</td><td>392 Ko</td><td>.gpkg</td>
    <td>-</td>
  </tr>
  <tr><td colspan="4" height=10px style="outline: "></td>
  <tr>
    <td>Jeu de données exemple (entraînement et test réduits)</td><td>1.6 Go/td><td>.zip</td>
    <td><a style="font-size: 10pt" href="https://storage.gra.cloud.ovh.net/v1/AUTH_366279ce616242ebb14161b7991a8461/defi-ia/flair_data_2/flair_2_toy_dataset.zip"><b>download</b></a></td>
  </tr>
</table>
</center>
<br/><br/>

</details>
<br><br>

### Citation

Si vous utilisez des données de FLAIR #2, merci d'inclure la citation suivante:

Texte brut:
```
Anatol Garioud, Nicolas Gonthier, Loic Landrieu, Apolline De Wit, Marion Valette, Marc Poupée, Sébastien Giordano and Boris Wattrelos. 2023. 
FLAIR: a Country-Scale Land Cover Semantic Segmentation Dataset From Multi-Source Optical Imagery. (2023). 
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
