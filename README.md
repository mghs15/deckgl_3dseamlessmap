# deckgl_3dseamlessmap
地理院地図Vectorのデータを、deck.glで3Dっぽくシームレスに表示するサンプル。

> [!TIP]
> blog: https://qiita.com/mg_kudo/items/6079ac10b7994e391228

> [!NOTE]
> 改良版レポジトリ https://github.com/mghs15/deckgl-3dmap-maplibre
> * ライブラリを最新化（2025/1月時点）
> * 標高タイルを用いて Z 値を付与
> * 水域や注記・記号も3次元風に表示可能

## 3Dサンプル
筑波山周辺の3Dデータを表示します。

https://mghs15.github.io/deckgl_3dseamlessmap/index.html

大きなデータがダウンロードされるのでご注意ください。
以下は、1度に表示されるデータを表示位置周辺のZL15のタイル4枚相当に制限したものです。

https://mghs15.github.io/deckgl_3dseamlessmap/index_limit.html


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


※データ自体は以下のレポジトリに移動しました。

https://github.com/mghs15/3dTiledJSON


## 参考にした資料
### データ
* 国土地理院 地理院地図Vector https://maps.gsi.go.jp/vector/
* 国土地理院 地理院タイル（標高タイル） https://maps.gsi.go.jp/development/ichiran.html#dem

### 利用ライブラリ
* deck.gl https://deck.gl/
* Mapbox GL JS https://docs.mapbox.com/mapbox-gl-js/api/
* Turf.js https://turfjs.org/

### ドキュメント等
* Slippy map tilenames https://wiki.openstreetmap.org/wiki/Slippy_map_tilenames
* MDN web docs (XMLHttpRequest) https://developer.mozilla.org/ja/docs/Web/API/XMLHttpRequest

※このレポジトリの元になった[deckgl_3dmap](https://github.com/mghs15/deckgl_3dmap)もご参照ください。
