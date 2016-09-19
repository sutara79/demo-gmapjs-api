# Googleマップをウェブページで利用する方法
現状では、マップ上でのスクロールを許可しない場合はAPIを、  
スクロールを許可する場合はインラインフレームを使うのが楽だと思います。

私個人としては、APIでスクロール無効に設定して使うのが気に入っています。

- - -
## デモ
http://sutara79.github.io/demo-gmapjs-api

- - -
## 関連ページ
- [APIキー管理画面](https://console.developers.google.com/apis/credentials)
- JavaScript API
    - [スタートガイド](https://developers.google.com/maps/documentation/javascript/tutorial?hl=ja)
    - [APIキーを取得](https://developers.google.com/maps/documentation/javascript/get-api-key?hl=ja)
    - [インフォウィンドウ作例](https://developers.google.com/maps/documentation/javascript/examples/infowindow-simple?hl=ja)
- Embed API
    - [デベロッパーガイド](https://developers.google.com/maps/documentation/embed/guide)

- - -
## ある住所をJavaScript APIで表示する方法

### 住所の緯度経度を取得
下記の2つの方法があります。

- [Geocoding - 住所から緯度経度を検索](http://www.geocoding.jp/)
- GoogleマップのURLのパラメータから抜き出す。  
  たとえば、Googleマップで「小倉城」と検索した場合、下記のようなURLになります。  
  `https://www.google.com/maps/place/%E5%B0%8F%E5%80%89%E5%9F%8E/@33.8831353,130.8755638,17z/data=!4m5!3m4!1s0x3543b8ad94500c23:0x1307eedef77d6d68!8m2!3d33.884431!4d130.874261?hl=ja`  
  `@33.8831353,130.8755638`は画面の中心となる座標であって、小倉城の座標ではありません。  
  末尾にある`!3d33.884431!4d130.874261`のうち、
  `!3d`と`!4d`を取り除いたものが、小倉城の座標です。  
  (緯度:`33.884431`、経度:`130.874261`)

- - -
## 関連ブログ記事
- [Googleマップをページに埋め込む手順 - すたらブログ](http://sutara79.hatenablog.com/entry/2016/07/07/145311)