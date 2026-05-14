# findposter

日本のオープンデータとGoogleマップを利用して、選挙ポスターの掲示場所や投票所を検索・可視化するウェブアプリケーションです。

![findposter スクリーンショット](http://fukuno.jig.jp/2014/findposter.jpg)

## 機能

- 選挙ポスターの掲示場所や投票所の位置をインタラクティブな地図上に可視化します。
- デバイスの位置情報を利用して、近くの場所を自動的に検索します。
- 「前へ」「次へ」「最短」のコントロールを使用して、最寄りのスポット間をナビゲートします。
- SPARQLを使用して日本のオープンデータプラットフォーム（ODP）からデータを取得します。

## はじめに

### 前提条件

このプロジェクトを動作させるには、Google Maps APIキーが必要です。キーを取得し、`lib/gmap.js`ファイルの`API_KEY`変数に設定してください。

```javascript
// lib/gmap.js
var API_KEY = "YOUR_GOOGLE_MAPS_API_KEY_HERE";
```

### アプリケーションの実行

1. リポジトリをローカルマシンにクローンします。
2. 上記の手順に従って、`lib/gmap.js`にGoogle Maps APIキーを追加します。
3. ウェブブラウザで`index.html`ファイルを開きます。
4. アプリケーションが位置情報の利用許可を求め、最寄りのスポットを表示します。

## データソース

このプロジェクトは、公開SPARQLエンドポイントを通じて日本のオープンデータプラットフォーム（ODP）からデータを取得します。

- **エンドポイント:** `https://sparql.odp.jig.jp/data/sparql`
- **クエリ対象のデータタイプ:**
    - `http://odp.jig.jp/odp/1.0#PosterPlace` （選挙ポスターの掲示場所）
    - `http://odp.jig.jp/odp/1.0#Polls` （投票所）

## クレジット

福野泰介（Taisuke Fukuno）氏によるオリジナル作品をベースにしています。
> (c)taisukef CC BY http://fukuno.jig.jp/

## ライセンス

MIT License — 詳細は [LICENSE](LICENSE) を参照してください。
