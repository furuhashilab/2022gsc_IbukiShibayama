# 2022gsc_IbukiShibayama
2022年度古橋卒論用レポジトリ
# PLATEAUの整備フローを基にした相模原キャンパスの3D都市モデル制作とオープンデータとしての利用 / Production of a 3D city model of Sagamihara campus based on the PLATEAU development flow 
and its use as Open Data

2022年度 卒論

青山学院大学 地球社会共生学部 地球社会共生学科

柴山息吹/IBUKI SHIBAYAMA

学生番号 1A119084

指導教員 古橋大地 教授

© Furuhashi Laboratory/Ibuki Shibayama, CC BY 4.0

## Abstract
国土交通省による3D都市モデルのプロジェクトである PLATEAU において、高精度な3D建物モデルの整備が進む都心エリアとその他の地域の整備状況の格差に注目し、市民参加型で進められるような整備方法を試験的に実践した。本研究では青山学院大学相模原キャンパスを対象に建物モデルを制作し、オープンデータとして公開した。

## Introduction
日本全国の3D都市モデルデータを整備し、オープンデータとして流通させる「Project PLATEAU」は国土交通省の主導で2020年度から開始された。都心部で高精度な3D建物モデルの整備が進む一方で、その他の地域では建物の高さのみが反映された「箱型モデル」にとどまっているという状況である。この課題に注目し、対策として市民参加型の3Dモデル整備を考案する。考案した整備フローは青山学院大学相模原キャンパスを対象に実践し、建物モデルを制作した後にオープンデータとして公開する。

## Methods
PLATEAUの整備フローを参考に、オープンデータのみを利用した3D建物モデルの整備フローを以下のように考案した。航空測量情報に対応させるデータとしてドローンのLiDARで取得した点群データを、そのデータをもとにフリーでオープンソースのソフトウェアであるBlenderでモデリングをする、というものである。市民参加型という前提から、無料かつGUIでモデル整備ができるように考慮している。出来上がったものはクリエイティブコモンズライセンスで公開し、誰でも二次利用ができるように設定する。

## Results
考案した整備フローを実践し、青山学院大学相模原キャンパスの建物のLOD2〜3相当のモデルが完成した。完成したモデルを、CC BY 4.0 のライセンスで GitHub、SketchfabにSTL、OBJ形式で公開した。

## Discussion
考案した整備フローで高精度な建物モデルを制作することができた。しかし、Blenderの操作の難易度や効率の悪さの面から、市民参加型で広範囲の地域のモデル整備を迅速に行うことは難しいと考えられる。点群データから自動でメッシュモデルを生成できるようなAIやツールを用いることで実現に近づけると感じた。

## Conclusion
ドローンで取得した点群データとBlenderのみで高精度な建物モデルを制作することができた。ただし、難易度や効率の観点からは市民参加型の整備フローとしての実現性は低いと言える。今後はAIやツールを用いながら自動で行う作業と、微調整などの手作業を組み合わせた整備フローが用いられることを見据え、その際に参考になるように今回の実践で気付いた点などをTipsとして公開する。また、オープンデータとして公開したキャンパスの3Dモデルが、ジャンルの垣根を越えてあらゆる場面で二次利用されることを期待している。

## Acknowledgements
本研究を進めるにあたり、青山学院大学 地球社会共生学部 [古橋大地教授](https://github.com/mapconcierge) にフィールドワークの機会や貴重な助言を賜りました。また、 [鈴木颯太氏](https://github.com/SotaSuzuki-1327) には屋内点群データの取得の協力を賜りました。深く感謝致します。

#### [昨年度のゼミ論レポジトリ](https://github.com/furuhashilab/2021gsc_IbukiShibayama)
#### 2022年度卒論 中間発表
* [Medium]()
* [スライド]()
#### Medium
#### スライド
#### 先行事例/既往研究
1. [PLATEAU](https://www.mlit.go.jp/plateau/?fbclid=IwAR2nENW2VCgIgpTdS7G2wIezhcJVmthRkynTP8YXiN8ybGT9Fkn_qOQpY6s)
2. [VR東大](https://vr.u-tokyo.ac.jp/virtualUT/)
3. [バーチャル渋谷](https://cluster.mu/w/79347fb9-05f5-429e-ab5f-8951ee8cd966)
#### 新規性
* 市民による3Dモデル整備の可能性を実践しながら検証する点。
* キャンパスの3Dモデルをオープンデータ化する点。
#### Advent Calendar
* ["3Dさがきゃん御三家公開" 2022/12/31](https://medium.com/furuhashilab/3d%E3%81%95%E3%81%8C%E3%81%8D%E3%82%83%E3%82%93%E5%BE%A1%E4%B8%89%E5%AE%B6%E5%85%AC%E9%96%8B-156222746e9a)
#### Sketchfab
* [ibukilego home](https://sketchfab.com/ibukilego)
* [Collection 青山学院大学 相模原キャンパス](https://skfb.ly/oCRWu)
## 参考文献リスト
https://docs.google.com/spreadsheets/d/1bJ8EX_SESjuZiktEz_Et8UpGBwUkUeSjRpzbrs9SqyI/edit?usp=sharing
