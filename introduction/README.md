# Blender 入門

* 制作環境 : Blender 2.79b 以降 / Ubuntu 16.04.4 LTS 以降
* .blend ファイルを開くには [Blender](https://www.blender.org/) が必要です。

### <b>INDEX</b>

|No.|タイトル|内容|.blend|参考サイト|
|:--:|:--|:--|:--:|:--:|
|001|[インストール](#インストール)|最新版のインストールと日本語化|－|－|
|002|[プリミティブ](#プリミティブ)|10種類のプリミティブの利用方法|－|－|
|003|[ユーザー設定](#ユーザー設定)|初期設定では使いにくい設定を変更|－|－|
|004|[入門動画](#入門動画)|入門者向けの解説動画|[●](#入門動画)|－|
|005|[『無料ではじめるBlender CGイラストテクニック』](#『CGイラストテクニック』)|参考書の勉強|[●](#『CGイラストテクニック』)|[●](https://amzn.to/2HUNroF)|
|006|[ショートカットキー](#ショートカットキー)|個人的に必須のショートカットキー|－|－|
|007|[マウス操作](#マウス操作)|個人的に必須のマウス操作|－|－|
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
|026|[スプリング（ばね）](https://www.youtube.com/watch?v=8UFcZBk6v9Y)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_026.blend)|－|2018-05-15|
|027|[歯車の作成とかみ合わせ](https://www.youtube.com/watch?v=iWRNMG9LAYY)|[●](https://vvestvillage.github.io/Blender/introduction/blend/004_027.blend)|[●](https://syoshinsya-3d.hatenablog.com/entry/2018/05/06/220800)|2018-05-21|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年04月20日  
更新日：2018年05月21日


<a name="『CGイラストテクニック』"></a>
# <b>005 『無料ではじめるBlender CGイラストテクニック』</b>

頁数は [『無料ではじめるBlender CGイラストテクニック／大澤龍一著』](https://amzn.to/2HUNroF) のページです。  
.blend ファイルを開くには [Blender](https://www.blender.org/) が必要です。

|No.|内容|頁数|.blend|参考サイト|作成日|
|:--|:--|:--:|:--:|:--:|:--:|
|001|プリミティブでキャラクターを作る|029|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_001.blend)|－|2018-05-07|
|002|プリミティブで木を作る|035|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_002.blend)|－|2018-05-07|
|003|ガラスのコップ（一部色付き）を作る|041|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_003.blend)|－|2018-05-08|
|004|細分割曲面で葉っぱを表現|051|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_004.blend)|－|2018-05-08|
|005|帽子をかぶったサボテン君|052|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_005.blend)|－|2018-05-08|
|006|イルカ（ミラー使用）|054|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_006.blend)|－|2018-05-08|
|007|お城|055|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_007.blend)|－|2018-05-09|
|008|さまざまな造形のアイデア|056|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_008.blend)|－|2018-05-09|
|009|取っ手･ブーリアン|063|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_009.blend)|－|2018-05-10|
|010|ナイフ･細分化･プロポーショナル編集|066|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_010.blend)|－|2018-05-10|
|011|ドロー系ソフトからの読み込み / メッシュに変換|076 / 086|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_011.zip)|－|2018-05-15|
|012|額縁（ベジェカーブと円カーブ）|084|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_012.blend)|－|2018-05-15|
|013|ヘビ（Alt+C→カーブからメッシュに変換）|086|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_013.blend)|－|2018-05-16|
|014|スクリュー|087|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_014.blend)|－|2018-05-17|
|015|シャワーヘッド（ブーリアン）|088|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_015.blend)|－|2018-05-17|
|016|スカルプトモデリング|095|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_016.blend)|－|2018-05-17|
|017|配列複製（直線 / カーブ）|105|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_017.blend)|[●](https://www.youtube.com/watch?v=-fzLGuckHh0)|2018-05-18|
|018|配列複製（格子）|107|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_018.blend)|－|2018-05-18|
|019|配列複製（ビル）|108|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_019.blend)|－|2018-05-18|
|020|パーティクルで大量複製配列の基本（植物）|109|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_020.blend)|－|2018-05-20|
|021|パーティクルヘアー（髪の毛）|117|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_021.blend)|－|2018-05-24|
|022|ソファーとぬいぐるみ|123|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_022.blend)|－|2018-05-25|
|023|ひまわり（ウェイトペント / パーティクル→メッシュに変換）|135|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_023.blend)|－|2018-05-29|
|024|やかん（別オブジェクトに分離）|141|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_024.blend)|－|2018-05-29|
|025|マテリアル（光沢BSDF / ガラスBSDF）|148|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_025.blend)|－|2018-05-29|
|026|マテリアルノード（ノードエディタ）|151|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_026.blend)|－|2018-05-29|
|027|よく使う4種類のマテリアル（艶あり / 艶あり / 金属 / ガラス）|156|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_027.blend)|－|2018-05-29|
|028|テクスチャ（フラット / ボックス / 球 / チューブ）|170|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_028.zip)|[●](https://www.textures.com/)|2018-05-30|
|029|汚れた感じを足す（grunge / smudge）|178|[●](https://vvestvillage.github.io/Blender/introduction/blend/005_029.zip)|[●](https://www.textures.com/)|2018-05-30|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年05月07日  
更新日：2018年05月30日


<a name="ショートカットキー"></a>
# <b>006 ショートカットキー</b>

他のソフトウェアとの兼ね合いもありショートカットキーは多用しません。

|ショートカットキー|内容|DATE|
|:--|:--|:--:|
|[Del]|選択したオブジェクトを削除する|2018-05-24|
|[Shift]+[s]|3Dカーソルの位置を原点に移動する等|2018-05-24|
|[A]|全選択 / 全選択解除|2018-05-24|5
|[Z]|ソリッド⇆ワイヤーフレーム表示|2018-05-24|
|[S]|拡大･縮小|2018-05-25|
|[E]|押し出しえ|2018-05-25|
|[B]|矩形で範囲指定|2018-05-25|
|[C]|ドラッグでｓ範囲指定|2018-05-25|
|[G]|自由移動（X･Y･Zの併用で方向限定）|2018-05-25|
|[R]|回転（X･Y･Zの併用で方向限定）|2018-05-25|
|[F10]|カメラの位置でビュー|2018-05-25|
|[Alt]+[C]|カーブなどからメッシュに変換|2018-05-25|
|[P]|別オブジェクトに分離|2018-05-29|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年05月24日  
更新日：2018年05月29日


<a name="マウス操作"></a>
# <b>007 マウス操作</b>

|マウス操作|内容|DATE|
|:--|:--|:--:|
|[右ボタン]|オブジェクトの選択|2018-05-24|
|[Shift]+[右ボタン]|オブジェクトの選択の追加 / 選択の解除|2018-05-24|
|[ホイール回転]|視点のズームアップ･ズームダウン（画面中央を基準）|2018-05-24|
|[中ボタン]+[ドラッグ]|視点の回転（選択したオブジェクトを基準）|2018-05-24|
|[Shift]+[中ボタン]+[ドラッグ]|視点の自由移動|2018-05-24|
|[Shift]+[ホイール回転]|視点の上下移動|2018-05-24|
|[Ctrl]+[ホイール回転]|視点の左右移動|2018-05-24|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：vvestvillage  
作成日：2018年05月24日  
更新日：2018年XX月XX日


© 2018 vvestvillage