# 2022gsc_IbukiShibayama
2022年度古橋卒論用レポジトリ
# PLATEAUの整備フローを基にした相模原キャンパスの3D都市モデル制作とオープンデータとしての利用 / Production of a 3D city model of Sagamihara campus based on the PLATEAU development flow and its use as Open Data

2022年度 卒論

青山学院大学 地球社会共生学部 地球社会共生学科

柴山息吹/IBUKI SHIBAYAMA

学生番号 1A119084

指導教員 古橋大地 教授

© Furuhashi Laboratory/Ibuki Shibayama, CC BY 4.0

## Abstract
国土交通省による3D都市モデルのプロジェクトである PLATEAU において、高精度な3D建物モデルの整備が進む都心エリアとその他の地域の整備状況の格差に注目し、市民参加型で進められるような整備方法を試験的に実践した。本研究では青山学院大学相模原キャンパスを対象に建物モデルを制作し、オープンデータとして公開した。

## Introduction
日本全国の3D都市モデルデータを整備し、オープンデータとして流通させる「Project PLATEAU」は国土交通省の主導で2020年度から開始された。都心部で高精度な3D建物モデルの整備が進む一方で、その他の地域では建物の高さのみが反映された「箱型モデル」にとどまっているという状況である。この課題に注目し、対策として市民参加型の3Dモデル整備を考案する。考案した整備フローは青山学院大学相模原キャンパスを対象に実践し、建物モデルを制作した後にオープンデータとして公開する。なお、本研究は [2021年度実施のゼミ論『PLATEAUの整備フローを基にした相模原キャンパスの建物3Dオープンデータの制作』](https://github.com/furuhashilab/2021gsc_IbukiShibayama) を継続、アップデートしたものである。

## Methods
PLATEAUの整備フローを参考に、オープンデータのみを利用した3D建物モデルの整備フローを以下のように考案した。航空測量情報に対応させるデータとしてドローンのLiDARで取得した点群データを、そのデータをもとにフリーでオープンソースのソフトウェアであるBlenderでモデリングをする、というものである。利用市民参加型という前提から、無料かつGUIでモデル整備ができるように考慮している。

* ドローンによるデータの取得は、2021年12月15日に相模原キャンパスにて古橋大地教授の主導の下 [Aero Sense 社製 Aerobo Wing AS-VT01](https://aerosense.co.jp/vtol-as-vt01) を使用して構内全域を対象に行った。

* また、今回は屋内のモデルも整備するために2023年12月26日にC棟チャペル内の一部のみを対象に、LiDAR 搭載の [Apple 社製 iPhone 12 Pro ](https://support.apple.com/kb/SP831?locale=ja_JP) で iOS 向けフリーアプリ [Scaniverse](https://scaniverse.com/) を利用してデータを取得した。

* 点群データは Las 形式でオープンソースソフトウェアの [CloudCompare](https://www.danielgm.net/cc/) にインポートし、点群の間引きとトリミングを行い、各棟ごとに切り分けたものを Ply 形式で [GitHub](https://github.com/furuhashilab/2021gsc_IbukiShibayama/tree/main/2021ply) に格納、公開した。Ply 形式にエクスポートした理由は、Blender へ直接インポートが可能になるからである。

* Blender に Ply データをインポートし、点群の分布に沿ってメッシュを手動で調整し、オブジェクトを作成した。
出来上がったものはクリエイティブコモンズライセンスで公開し、誰でも二次利用ができるように設定する。今回は3Dモデルを用いた仮想空間の作成、3Dプリントを実践し、二次利用の例として提示する。

* モデリング対象は、相模原キャンパス内で名前に "棟" が付く19の建物または施設とする。ただし J、K、L 棟はまとめてモデリング、公開する。
  * 資料2: 青山学院大学相模原キャンパスマップ (出典: キャンパスマップ, 青山学院大学, https://www.aoyama.ac.jp/outline/campus/sagamihara.html)
<img width="50%" alt="gr20220823" src="https://user-images.githubusercontent.com/72287333/216678418-c9686a71-1807-46bc-8fe5-1a651e7ed252.svg">


## Results
考案した整備フローを実践し、青山学院大学相模原キャンパス内対象の建物のLOD2〜3相当のモデルが完成した。完成したモデルを、CC BY 4.0 のライセンスで [GitHub](https://github.com/furuhashilab/2022gsc_IbukiShibayama/tree/main/tmp) にSTL、[Sketchfab](https://sketchfab.com/ibukilego) にOBJ形式で公開した。

### A棟 (2022/12公開)
<img width="50%" alt="2023-02-04" src="https://user-images.githubusercontent.com/72287333/216691424-aa7bc582-7372-43dd-a7cd-5e9fc84213c5.png">

### B棟 (2022/11公開)
<img width="50%" alt="2023-02-04 (1)" src="https://user-images.githubusercontent.com/72287333/216691791-e2e6f5d2-4fb6-4bcf-ba31-6bc0c50a88ca.png">

### C棟 (2021/2公開)
<img width="50%" alt="2023-02-04 (2)" src="https://user-images.githubusercontent.com/72287333/216691953-9cd7f4c6-c340-4743-940e-d7f2d0e3e68c.png">

### D棟 (2023/1公開)
<img width="50%" alt="2023-01-31 (1)" src="https://user-images.githubusercontent.com/72287333/216691993-922aaddd-3c7f-4c16-9e37-2465db9f7d20.png">

### E棟 (2023/1公開)
<img width="50%" alt="2023-01-27" src="https://user-images.githubusercontent.com/72287333/216692079-5824b180-3b49-4f4c-86c0-aa9b16d00a6e.png">

### F棟 (2023/1公開)
<img width="50%" alt="2023-01-19" src="https://user-images.githubusercontent.com/72287333/216692098-dc88d439-1e33-460c-ad42-f15be3f74fcd.png">

### G棟 (2023/2公開)
<img width="50%" alt="2023-02-02" src="https://user-images.githubusercontent.com/72287333/216692111-fcd3c5f3-16d3-4d24-874f-b7c8032165fb.png">

### H棟 (2023/2公開)
<img width="50%" alt="2023-02-03" src="https://user-images.githubusercontent.com/72287333/216692149-ecd6ff93-3111-4199-ab52-da1919737df7.png">

### I棟 (2023/2公開)
<img width="50%" alt="2023-02-03 (4)" src="https://user-images.githubusercontent.com/72287333/216692189-e22d51fb-85df-4bc4-9041-48c7ea8c8158.png">

### J, K, L棟 (2023/1公開)
<img width="50%" alt="2023-01-06" src="https://user-images.githubusercontent.com/72287333/216692309-a6ee48b6-1d24-4d79-923e-2cfac8f79a78.png">

### M棟 (2023/2公開)
<img width="50%" alt="2023-02-03 (3)" src="https://user-images.githubusercontent.com/72287333/216692334-2fe47954-9dca-45ab-89f8-a7062ce52382.png">

### N棟 (2023/2公開)
<img width="50%" alt="2023-02-02 (1)" src="https://user-images.githubusercontent.com/72287333/216692362-c31bb8b5-0730-4548-8bcc-e16cf6d99398.png">

### O棟 (2023/2公開)
<img width="50%" alt="2023-02-01" src="https://user-images.githubusercontent.com/72287333/216692381-6b70b7ee-fb94-4a39-abb4-93721d9ada7b.png">

### P棟 (2023/2公開)
<img width="50%" alt="2023-02-03 (2)" src="https://user-images.githubusercontent.com/72287333/216692414-c18432a1-122e-4044-852a-dd10ad79b740.png">

### R棟 (2023/2公開)
<img width="50%" alt="2023-02-03 (1)" src="https://user-images.githubusercontent.com/72287333/216692474-b8b5604d-5987-49b5-bd79-07aded83dbc6.png">

### S棟 (2023/2公開)
<img width="50%" alt="2023-02-03 (6)" src="https://user-images.githubusercontent.com/72287333/216692507-50dd3eed-26ab-4fd3-9723-75f5539f6cbc.png">

### V棟 (2023/2公開)
<img width="50%" alt="2023-02-03 (5)" src="https://user-images.githubusercontent.com/72287333/216692548-25721ee7-9611-4ba0-83c3-b5aae5744418.png">

対象全ての棟の Stl ファイルの3Dプリントも完了した。FlashPrint にロードすると、オブジェクトのサイズが Blender の 1/1000 になった。さらにスライス時に50%のサイズに調整しているので、最終的にプリントされるモデルのスケールは 1/2000 となる。

<img width="50%" alt="IMG_20230204_041151" src="https://user-images.githubusercontent.com/72287333/216693710-ff658315-055b-4dba-9519-b38d7a77ca95.jpg">

<img width="50%" alt="IMG_20230204_041129" src="https://user-images.githubusercontent.com/72287333/216693987-a1e69408-15b9-4dac-8fa4-a4d5d00106f9.jpg">

<img width="50%" alt="IMG_20230204_041303" src="https://user-images.githubusercontent.com/72287333/216694897-a0c6c994-8e12-49a5-91e9-9318d3b3096c.jpg">

また、C棟チャペルの屋内の点群データから1階礼拝室の3Dモデルのプロトタイプを制作し、Glich でVR実装し公開した。

<img width="50%" alt="2023-02-04 (3)" src="https://user-images.githubusercontent.com/72287333/216698810-38ffaac1-1a76-4687-a42e-a4c9e1c681dd.png">

* VR
  * https://trite-voracious-cuticle.glitch.me
* AR

## Discussion
* 考案した整備フローで高精度な建物モデルを制作することができた。しかし、Blenderの操作の難易度や効率の悪さの面から、市民参加型で広範囲の地域のモデル整備を迅速に行うことは難しいと考えられる。点群データから自動でメッシュモデルを生成できるようなAIやツールを用いることで実現に近づけると感じた。

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
