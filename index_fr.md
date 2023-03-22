---
title: Challenge Flair
---
# Bienvenue sur la page des datasets FLAIR de l'IGN

<p align="center"><img src="img/flair_logo.jpg" alt="" width="40%" /></p>


<a style="font-size: 11pt" href="./index.html"><b>English version</b></a>

<br>

L'Institut national de l'information géographique et forestière (IGN) présente ses défis en matière d'IA et ses jeux de données de référence FLAIR (pour French Land Cover from Aerospace ImageRy). [En savoir plus sur le contexte de ces défis.](./pourquoi_flair.html) 

<hr><p align="center"><img src="img/visuel_FLAIR_bandeau.jpg" alt="" width="100%" /></p>
<hr>
You can reach us at : <a href = "mailto:ai-challenge@ign.fr?subject=FLAIR - AI challenge @IGN">ai-challenge@ign.fr</a>
<br><br>

## FLAIR #1 : segmentation sémantique et adaptation de domaine

<img src="img/logo_ign_sfpt.png" alt="" width="30%" />

Ce challenge s'est déroulé du 21 Novembre 2022 au 21 Mars 2023. Vous pouvez consulter les résultats <a style="font-size: 10pt" href="https://codalab.lisn.upsaclay.fr/competitions/8769"><b>ici.</b></a><br/>

FLAIR #1 <b> datapaper  &#128209;</b>  : https://arxiv.org/pdf/2211.12979.pdf <br>
FLAIR #1 <b> dépôt github &#128193;</b> : https://github.com/IGNF/FLAIR-1-AI-Challenge<br>

### Description

Avec des données acquises sur 50 départements et plus de 20 milliards de pixels annotés, ce jeu de données représente la diversité du territoire métropolitain, ses climats, ses écosystèmes et ses sols, dans le but de produire une cartographie à grande échelle. Différentes bases de données IGN (BD Ortho, RGE Alti) ainsi que des annotations produites manuellement par des experts photo-interprètes ont été assemblées pour permettre l’entraînement de modèles IA.

Les images aériennes de télédétection à l'échelle d'un pays sont nécessairement acquises à des dates et des heures différentes et dans des conditions différentes. De même, à grande échelle, les caractéristiques des classes sémantiques peuvent varier et devenir hétérogènes. Cela soulève des challenges pour la généralisation spatiale et temporelle des modèles d'apprentissage profond !

Le dataset FLAIR#1 est composé de 77,412 patches de 512x512 (résolution spatiale de 0.2m) avec une sémantique à 19 classes. Spécifiquement pour le challenge et les baselines associées et en raison d'une fréquence par classe déséquilibrée, la sémantique a été modifiée à 13 classes (>12 -> 13). Rapportez-vous au datapaper pour plus de précisions. 

<center>
<table style="width:50%">
<thead>
  <tr><th width=20%></th><th>Classe</th><th width=15%>Valeur</th></tr>
</thead>
<tbody>
  <tr><td bgcolor='#db0e9a'></td><td>bâtiment</td><td>1</td></tr>
  <tr><td bgcolor='#938e7b'></td><td>zone perméable</td><td>2</td></tr>
  <tr><td bgcolor='#f80c00'></td><td>zone imperméable</td><td>3</td></tr>
  <tr><td bgcolor='#a97101'></td><td>sol nu</td><td>4</td></tr>
  <tr><td bgcolor='#1553ae'></td><td>eau</td><td>5</td></tr>
  <tr><td bgcolor='#194a26'></td><td>conifères</td><td>6</td></tr>
  <tr><td bgcolor='#46e483'></td><td>feuillus</td><td>7</td></tr>
  <tr><td bgcolor='#f3a60d'></td><td>brousaille</td><td>8</td></tr>
  <tr><td bgcolor='#660082'></td><td>vigne</td><td>9</td></tr>
  <tr><td bgcolor='#55ff00'></td><td>pelouse</td><td>10</td></tr>
  <tr><td bgcolor='#fff30d'></td><td>culture</td><td>11</td></tr>
  <tr><td bgcolor='#e4df7c'></td><td>terre labourée</td><td>12</td></tr>
  <tr><td bgcolor='#3de6eb'></td><td>piscine</td><td>13</td></tr>
  <tr><td bgcolor='#ffffff'></td><td>neige</td><td>14</td></tr>
  <tr><td bgcolor='#8ab3a0'></td><td>coupe</td><td>15</td></tr>
  <tr><td bgcolor='#6b714f'></td><td>mixte</td><td>16</td></tr>
  <tr><td bgcolor='#c5dc42'></td><td>ligneux</td><td>17</td></tr>
  <tr><td bgcolor='#9999ff'></td><td>serres</td><td>18</td></tr>
  <tr><td bgcolor='#000000'></td><td>autre</td><td>19</td></tr>
</tbody>
</table>
</center>

Le dataset couvre un total d'environ 800 km², avec des patches sélectionnés sur l'ensemble du territoire métropolitain afin de représenter sa diversité (domaines spatiaux). Les images aériennes incluent dans le dataset sont également acquisent à des mois et années différentes (domaines temporels). 

<table>
    <tr>
        <td style="text-align: center"><img src="img/ortho.png" 
            alt="ORTHO HR" title="Michael Jordan" /></td>
        <td style="text-align: center"><img src="img/labels.png" alt="James Worthy" 
            title="Labels" /></td>
    </tr>
    <tr>
        <td style="text-align: center">ORTHO HR&#174;</td>
        <td style="text-align: center">Annotations</td>
    </tr>
</table>

Le dataset de test contient 15,700 patches de 10 domaines spatiaux supplémentaires. La fréquence des classes et les domaines temporels sont également distinct du dataset d'entraînement, permettant d'analyser les capacités de généralisation et d'adaptation de domaines des méthodes développées.


### Baseline model

Une architecture U-Net avec un encodeur ResNet34 pré-entraîné de la librairie segmentation-models-pytorch a été utilisée pour les baselines. L'architecture utilisée permet l'intégration d'informations de métadonnées à l'échelle du patch et utilise des techniques d'augmentation des données d'image couramment utilisées. Les codes sont disponibles dans le dépôt FLAIR #1.

### Datasets


<table>
  <tr>
    <th>Données</th>
    <th>Volume</th>
    <th>Type</th>
    <th>Lien</th>
  </tr>
  <tr>
    <td>Images aériennes</td>
    <td>xx Go</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr>
    <td>Métadonnées aériennes</td>
    <td>xx Mo</td>
    <td>.json</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr>
    <td>Annotations</td>
    <td>xx Go</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
  <tr>
    <td>Jeu de données réduit</td>
    <td>xx Mo</td>
    <td>.zip</td>
    <td><a style="font-size: 10pt" href=""><b>download</b></a>
  </tr>
</table>



<br><br>

## FLAIR #2 : Texture et temps à partir d'imagerie optique multimodal pour la segmentation sémantique 

<img src="img/logo_ign_cnes.png" alt="" width="30%" />

<b>Prochainement !</b> 

<!---
FLAIR #2 repository : https://github.com/IGNF/FLAIR-2-AI-Challenge
-->
