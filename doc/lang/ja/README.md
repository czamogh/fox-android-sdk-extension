[![Platform](http://img.shields.io/badge/platform-Android-green.svg?style=flat)](https://developer.android.com)
[![Language](http://img.shields.io/badge/language-java-red.svg?style=flat)](https://java.com)
[![F.O.X](http://img.shields.io/badge/F.O.X%20SDK-4.0.0%20〜-blue.svg?style=flat)](https://github.com/cyber-z/public-fox-android-sdk/blob/master/4.x/lang/ja/README.md)

# Force Operation X Android SDK Extension

本SDKは、Force Operation X Android SDKによる計測機能を拡張するためのプラグインモジュールとなります。<br>
利用するには[`F.O.X Android SDK 4.0.0`](https://github.com/cyber-z/public-fox-android-sdk/blob/master/4.x/lang/ja/README.md)以上を導入する必要があります。<br>
尚、本プラグインはオープンソースとなっておりますので改変しご利用頂いても構いません。

* **[1. サポートする機能](#support_functions)**
* **[2. インストール](#install_module)**
* **[3. イベントの計測](#event_extension)**

<div id="support_functions"></div>
## 1. サポートする機能

|種類|機能|詳細|
|:---:|:---|:---|
|Native|アプリ内の各種イベントの計測用拡張クラス|・ホーム画面表示イベント<br>・商品閲覧イベント<br>・複数商品閲覧イベント<br>・買い物かご閲覧イベント<br>・商品購入イベント<br>・レベルアップイベント<br>・カテゴリページイベント<br>・チュートリアル完了イベント<br>・検索イベント|
|Cocos2d-x|広告効果計測|F.O.X Android SDKのCocos2d-x用ラッパーの提供|
|Unity|リエンゲージメント計測|リエンゲージメント計測を実施するための計測用Activityクラスの提供|

<div id="install_module"></div>
## 2. インストール

build.gradleに以下の設定を追加します。

```
repositories {
    maven {
        url "https://github.com/cyber-z/public-fox-android-sdk/raw/master/mavenRepo"
    }
}

dependencies {
    compile 'co.cyberz.fox:foxtrack-core:4.0.0'
    compile 'co.cyberz.fox.support:foxtrack-extension:1.0.0'
}
```

> ※ 本プラグインを利用するには`F.O.X Android SDK 4.0.0`以上が導入されていることが条件となります。

<div id="event_extension"></div>
## 3. イベントの計測

本プラグインでは、アプリ内で発生する各種イベント別に必要となる計測パラメータの指定を<br>
簡易化するためのイベント拡張クラスを用意しています。<br>
プラグインでサポートしているアプリ内イベントは以下の通りです。

> #### 1. [ViewToppage(ホーム画面表示)イベント](./track_events/01_view_toppage/README.md)
> #### 2. [ViewProduct(商品閲覧)イベント](./track_events/02_view_product/README.md)
> #### 3. [ViewListing(複数商品閲覧)イベント](./track_events/03_view_listing/README.md)
> #### 4. [ViewBasket(買い物かご閲覧)イベント](./track_events/04_view_basket/README.md)
> #### 5. [TrackTransaction(商品購入)イベント](./track_events/05_track_transaction/README.md)
> #### 6. [AchieveLevel(レベルアップ)イベント](./track_events/06_achieve_level/README.md)
> #### 7. [ViewCategory(カテゴリページ)イベント](./track_events/07_view_category/README.md)
> #### 8. [TutorialCompletion(チュートリアル)イベント](./track_events/08_tutorial_completion/README.md)
> #### 9. [Search(検索)イベント](./track_events/09_search/README.md)

[**イベント計測の詳細**](./track_events/README.md)