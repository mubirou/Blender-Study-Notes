# Blender

この項目は、編集中の項目です。

* 制作環境 : Blender 2.79b 以降 / Ubuntu 16.04.4 LTS 以降
* .blend ファイルを開くには [Blender](https://www.blender.org/) が必要です
* .fbx ファイルは [Unity](https://store.unity.com/ja/) へのインポート用です

### <b>INDEX</b>

|No.|タイトル|内容|.blend|.fbx|
|:--:|:--|:--|:--:|:--:|
|001|[インストール](#インストール)|最新版のインストールと日本語化|－|－|
|002|[プリミティブ](#プリミティブ)|10種類のプリミティブの利用方法|－|－|
***

<a name="インストール"></a>
# <b>001 インストール</b>

### 概要
「Ubuntuソフトウェア」からインストールしたBlenderはバージョンが古い上、日本語化すると文字化けするため、以下の方法でインストールを行います。

### Blenderのインストール
端末を起動し、次の通りの処理を行います。
```
sudo add-apt-repository ppa:thomas-schiex/blender
sudo apt-get update
sudo apt-get install blender
```

### Blenderの日本語化
1. [File]-[User Preferences...] を開く。
1. [System]-[International Fonts] を [✔]。
1. [Languages] を [Japanes(日本語)] に変更。
1. [Translate] の [Interface]、[Tooltips]、[new Data] を選択。

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：Takashi Nishimura  
作成日：2018年04月18日

© 2018 Takashi Nishimura


<a name="プリミティブ"></a>
# <b>002 プリミティブ</b>

### 作成方法
1. 左端の [作成] タブを選択。
1. [メッシュ] の ①平面 ②立方体 ③円 ④UV球 ⑤ICO球 ⑥円柱 ⑦円錐 ⑧トーラス ⑨グリッド ⑩モンキー の中から選択。

### プリミティブ（メッシュ）の種類
1. 平面（Plane）
    * 頂点数4。
1. 立方体（Cube）
    * 頂点数8。
1. 円（Circle）
    * 辺のみ（色塗りはなし）。
    * 頂点数32。
1. UV球（UV Sphere）
    * 経度･緯度をポリゴンで分割されている球。
    * 頂点数482（見た目は綺麗）。
1. ICO球（Ico Sphere）
    * 三角ポリゴンで構成されている球。
    * 頂点数42（ポリゴン数は少ない）。
1. 円柱（Cylinder）
    * 頂点数64。
1. 円錐（Cone）
    * 頂点数33。
1. トーラス（Torus）
    * 頂点数576。
1. グリッド（Grid）
    * 頂点数100。
1. モンキー（Monkey）
    * Suzannu（スザンヌ）というBlenderのマスコットキャラ。
    * 頂点数507。

![002](https://takashinishimura.github.io/Blender/jpg/002.jpg)

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：Takashi Nishimura  
作成日：2018年04月19日

==========================================================================================
<a name="ユーザー設定"></a>
# <b>003 ユーザー設定</b>

* 初期設定では使いにくい設定を変更します。

### インターフェイス
* [ファイル]-[ユーザー設定]-[インターフェイス]
    * [カーソル深度] の [✔] を外す……中心が設定しにくくなる為
    * [選択範囲を中心に回転] に [✔]……見たいものを見失わないようにする為

### 入力
* [ファイル]-[ユーザー設定]-[入力]
    * [3ボタンマウスを再現] に [✔]……中ボタン→ [Alt] キー+ドラッグで代用する為
    * [テンキーを模倣] に [✔]……テンキー→数字キーで代用する為

### ファイル
* [ファイル]-[ユーザー設定]-[ファイル]

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：Takashi Nishimura  
作成日：2018年04月20日


© 2018 Takashi Nishimura