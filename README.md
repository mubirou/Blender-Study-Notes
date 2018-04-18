# Blender

* 制作環境 : Blender 2.79b 以降 / Ubuntu 16.04.4 LTS 以降
* .blend ファイルを開くには [Blender](https://www.blender.org/) が必要です
* .fbx ファイルは [Unity](https://store.unity.com/ja/) へのインポート用です

この項目は、編集中の項目です。

### <b>INDEX</b>

|No.|タイトル|内容|.blend|.fbx|
|:--:|:--|:--|:--:|:--:|
|001|[インストール](#インストール)|最新版のインストールと日本語化|－|－|
|002|xxxxx|xxxxx|－|－|
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