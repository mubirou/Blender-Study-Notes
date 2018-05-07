# Blender 入門

この項目は、編集中の項目です。

* 制作環境 : Blender 2.79b 以降 / Ubuntu 16.04.4 LTS 以降
* .blend ファイルを開くには [Blender](https://www.blender.org/) が必要です。

### <b>INDEX</b>

|No.|タイトル|内容|.blend|参考サイト|
|:--:|:--|:--|:--:|:--:|
|001|[インストール](#インストール)|最新版のインストールと日本語化|－|－|
|002|[プリミティブ](#プリミティブ)|10種類のプリミティブの利用方法|－|－|
|003|[ユーザー設定](#ユーザー設定)|初期設定では使いにくい設定を変更|－|－|
|004|[入門動画](#入門動画)|入門者向けの解説動画|[●](#入門動画)|－|
|005|[『無料ではじめるBlender CGイラストテクニック／大澤龍一著』](#『CGイラストテクニック』)|参考書|[●](#『CGイラストテクニック』)|[●](https://amzn.to/2HUNroF)|
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
作成者：vvestvillage  
作成日：2018年04月18日


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

![002](https://vvestvillage.github.io/Blender/introduction/jpg/002.jpg)

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年04月19日


<a name="ユーザー設定"></a>
# <b>003 ユーザー設定</b>

初期設定では使いにくい設定を変更します。

1. [ファイル]-[ユーザー設定]-[インターフェイス]
    * [カーソル深度] の [✔] を外す……中心が設定しにくくなる為
    * [選択範囲を中心に回転] に [✔]……見たいものを見失わないようにする為

1. [ファイル]-[ユーザー設定]-[入力]
    * [テンキーを模倣] に [✔]……テンキー→数字キーで代用する為

1. [透視投影]→[並行投影] に変更……正確な位置を把握しやすくする為（テンキー5で切替）

1. 単位を [単位プリセット]→[メートル] に変更  
![003_1](https://vvestvillage.github.io/Blender/introduction/jpg/003_1.jpg)

1. [左クリック] で [Lamp] を選択→ [ポイント]→[サン] に変更……使用頻度が高い為  
![003_2](https://vvestvillage.github.io/Blender/introduction/jpg/003_2.jpg)

1. [ファイル]-[スタートアップファイルの保存] を選択……次回起動時にも反映させる為

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年04月20日


<a name="入門動画"></a>
# <b>004 入門動画</b>

.blend ファイルを開くには [Blender](https://www.blender.org/) が必要です。

|No.|内容|.blend|参考サイト|視聴日|
|:--|:--|:--:|:--:|:--:|
|001|[画面操作･オブジェクトの操作･3Dカーソル](https://www.youtube.com/watch?v=du0ybLqScJk&index=1&list=PLmVkGpfcCZalGLfi3B5lx038GY1rNw2-L)|－|－|2018-04-20|
|002|[基本操作法（オブジェクトモード･編集モード）](https://www.youtube.com/watch?v=xgsTa-yiPHY)|－|－|2018-04-20|
|003|[機能紹介その①（基本動作）](https://www.youtube.com/watch?v=EHAgiNVKIPo)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_003.blend)|－|2018-04-20|
|004|[機能紹介その②（オブジェクトの色･アニメーション作成）](https://www.youtube.com/watch?v=KLm5B98zQV8)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_004.blend)|－|2018-04-21|
|005|[3Dテキストの作成](https://www.youtube.com/watch?v=3Jh_-HqSzmI)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_005.blend)|－|2018-04-21|
|006|[平面ライトの作り方](https://www.youtube.com/watch?v=dfoRfwacDSA)|－|－|2018-04-22|
|007|[綺麗なゴールドの設定](https://www.youtube.com/watch?v=DP1qJJkHmOQ)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_007.zip)|－|2018-04-22|
|008|[G･R･S + X･Y･Z + Ctrl](https://www.youtube.com/watch?v=RIR5p28CiZ4)|－|－|2018-04-22|
|009|[立方体からの変形（1･3･5 / E / B）](https://www.youtube.com/watch?v=wftv5exmsho)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_009.blend)|－|2018-04-23|
|010|[犬の作成①](https://www.youtube.com/watch?v=pkvMiEeJGro)･[②](https://www.youtube.com/watch?v=DUp9XAM42Cg)･[③](https://www.youtube.com/watch?v=sTdziqcgNnM)（A / B / Ctrl+R）|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_010_01.blend)[●](https://vvestvillage.github.io/Blender/introduction/blend/004_010_02.blend)[●](https://vvestvillage.github.io/Blender/introduction/blend/004_010_03.blend)|－|2018-04-25|
|011|[UVマッピング](https://www.youtube.com/watch?v=IXXN3p8aCIM)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_011.zip)|－|2018-04-26|
|012|[ボーン（アーマチュア）の基本](https://www.youtube.com/watch?v=JULer0rGUBk)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_012.blend)|[●](https://yugalab.net/archives/2446)|2018-04-27|
|013|[ロゴアニメーション](https://www.youtube.com/watch?v=UBbkLTwx5WY)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_013.blend)|－|2018-04-28|
|014|[テキストに日本語を使う方法](https://www.youtube.com/watch?v=ISUJ8s_cHbM)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_014.blend)|－|2018-04-29|
|015|[20世紀フォックス風オープニング](https://www.youtube.com/watch?v=4iLOzG3eFh4)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_015.blend)|－|2018-04-29|
|016|[透明カップと布](https://www.youtube.com/watch?v=SSpoeL45oZ4)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_016.blend)|－|2018-04-30|
|017|[物理演算とオブジェクトの破壊](https://www.youtube.com/watch?v=fXMNR2InZqI)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_017.blend)|－|2018-05-02|
|018|[衝突破壊](https://www.youtube.com/watch?v=7wQ4bH499wU)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_018.blend)|－|2018-05-02|
|019|[基本ショートカット + Bool Tools](https://www.youtube.com/watch?v=g1E4N-osxQU)|－|－|2018-05-03|
|020|[カーブオブジェクト](https://www.youtube.com/watch?v=pYfRXz0tSBk)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_020.blend)|－|2018-05-04|
|021|[ワイングラス風](https://www.youtube.com/watch?v=rpdfeQRKSMg)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_021.blend)|－|2018-05-05|
|022|[カメラの設定](https://www.youtube.com/watch?v=ygrNtWcvoUg)|－|－|2018-05-06|
|023|[カメラのトラッキング](https://www.youtube.com/watch?v=Vu2Rtpuk6Aw)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_023.blend)|－|2018-05-06|
|024|[パスアニメーション](https://www.youtube.com/watch?v=4LpDGe-MpLE)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_024.blend)|－|2018-05-07|
|025|[流体シュミレーション](https://www.youtube.com/watch?v=inyfz4WsJt4)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_025.blend)|[●](https://blender-cg.net/fluid/)|2018-05-07|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年04月20日  
更新日：2018年05月07日


<a name="『CGイラストテクニック』"></a>
# <b>005 『CGイラストテクニック』</b>

[『無料ではじめるBlender CGイラストテクニック／大澤龍一著』](https://amzn.to/2HUNroF) を参考。  
.blend ファイルを開くには [Blender](https://www.blender.org/) が必要です。

|No.|内容|頁数|.blend|
|:--|:--|:--:|:--:|
|001|XXXXX|－|－|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年05月07日  
更新日：2018年XX月XX日

© 2018 vvestvillage