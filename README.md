# deckgl_3dseamlessmap
地理院地図Vectorのデータを、deck.glで3Dっぽくシームレスに表示するサンプル。

## 3Dサンプル
筑波山周辺の3Dデータを表示します。1度に表示されるのは、表示位置周辺のZL15のタイル4枚相当のデータです。

https://mghs15.github.io/deckgl_3dseamlessmap/index.html

## 作成
以下のレポジトリをベースに、3D用のデータをタイル状に分割し、表示範囲に合わせて読み込むようにした地図。

deckgl_3dmap
https://github.com/mghs15/deckgl_3dmap

データ作成には、以下のツールを利用。

https://mghs15.github.io/deckgl_3dseamlessmap/indexGet.html

タイル状に分割されたデータのパスは、とりいそぎ、以下の通り。

```data/{z}-{x}-{y}-1.json```

* {z}、{x}、{y}は、XYZタイル（Slippy map tilenames）方式に準ずる。
* 現状、サンプルサイトでは、全てのZLで、{z}=15を読み込む。

## 参考にした資料
### データ
* 国土地理院 地理院地図Vector https://maps.gsi.go.jp/vector/

### 利用ライブラリ
* deck.gl https://deck.gl/
* Mapbox GL JS https://docs.mapbox.com/mapbox-gl-js/api/
* Turf.js https://turfjs.org/

### ドキュメント等
* Slippy map tilenames https://wiki.openstreetmap.org/wiki/Slippy_map_tilenames
* MDN web docs (XMLHttpRequest) https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest

※このレポジトリの元になった[deckgl_3dmap](https://github.com/mghs15/deckgl_3dmap)もご参照ください。
