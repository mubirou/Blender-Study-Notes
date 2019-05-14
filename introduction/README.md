# Blender 入門

* 制作環境 : Blender 2.79b 以降 / Ubuntu 16.04.4 LTS 以降
* .blend ファイルを開くには [Blender](https://www.blender.org/) が必要です
* サンプル画像は異なるバージョンで制作されたものが混在しています

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
|008|[アドオン](#アドオン)|さまざなまな機能を追加|－|－|
|009|[ルーティンワーク](#ルーティンワーク)|制作時に毎回行うルーティン|－|－|
|010|[『はじめてのBlender（アニメーション編）』](#『はじめてのBlender』)|参考書の勉強|[●](#『はじめてのBlender』)|[●](https://amzn.to/2JiTi70)|
|011|[Unity用データ](#Unity用データ)|Unityで利用するためのポイント|－|－|
|012|[『Blender 3DCG モデリング･マスター』](#『モデリングマスター』)|参考書の勉強|[●](#『モデリングマスター』)|[●](https://amzn.to/2A2595W)|
|013|[『ブレンダーからはじめよう!』](#『ブレンダーからはじめよう!』)|参考書の勉強|[●](#『ブレンダーからはじめよう!』)|[●](https://amzn.to/2vzog2t)|
|014|[テクニック･ヒント1](#テクニック･ヒント1)|参考：[『Blender モデリング･マスター』](#『モデリングマスター』)|[●](#テクニック･ヒント1)|[●](https://amzn.to/2A2595W)|
|015|[テクニック･ヒント2](#テクニック･ヒント2)|参考：[『Blender CGイラストテクニック』](#『CGイラストテクニック』)|[●](#テクニック･ヒント2)|[●](https://amzn.to/2HUNroF)|
|016|[テクニック･ヒント3](#テクニック･ヒント3)|参考：アニメーション関連書籍（[●](#『はじめてのBlender』)[●](#『ブレンダーからはじめよう!』)）|[●](#テクニック･ヒント3)|[●](https://amzn.to/2JiTi70)[●](https://amzn.to/2vzog2t)|
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
1. […Font] を "/usr/share/fonts/opentype/noto/**Noto**SansCJK-Regular.ttc" に指定
1. [Translate] の [Interface]、[Tooltips]、[new Data] を選択。
1. [ユーザー設定の保存] ボタンを押す

### 参考：Blender 2.80 Betaの場合
1. https://www.blender.org/ にアクセス
1. [Get Blender 2.80-beta] をクリック
1. [Download Blender 2.8 Beta] をクリック
1. [2.80 Beta Linux 64bit] を選択→ダウンロード開始
1. ダウンロードされた圧縮ファイルを解凍→展開
1. 展開したフォルダ内の[blender]アイコンをダブルクリック→起動
1. [日本語化] する
    1. [Edit]-[Preferences]-[Interface]-[Translation] を次の通りに設定
        * Language（言語）：Japanese（日本語）
        * Tooltips（ツールチップ）：✔
        * Interface（インターフェイス）：✔
        * NewData（新規データ）：✔
    1. 引き続き [Text Renderring] のフォントを次の通りにする（任意）
        * Interface Font（UI用フォント）：/usr/share/fonts/opentype/noto/NotoSansCJK-Regular.ttc
        * Mono-space Font（等幅フォント）：（空白）←設定によってはPythonコンソールで不具合が生じる

実行環境：Blender 2.79b / 2.80 Beta、Ubuntu 18.04.X LTS  
作成者：夢寐郎  
作成日：2018年04月18日  
更新日：2019年03月09日 Ver.2.80 対応


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

![002](https://mubirou.github.io/Blender/introduction/jpg/002.jpg)

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
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
![003_1](https://mubirou.github.io/Blender/introduction/jpg/003_1.jpg)

1. [左クリック] で [Lamp] を選択→ [ポイント]→[サン] に変更……使用頻度が高い為  
![003_2](https://mubirou.github.io/Blender/introduction/jpg/003_2.jpg)

1. [ファイル]-[**スタートアップファイルの保存**] を選択……次回起動時にも反映させる為

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
作成日：2018年04月20日


<a name="入門動画"></a>
# <b>004 入門動画</b>

.blend ファイルを開くには [Blender](https://www.blender.org/) が必要です。

|No.|内容|.blend|参考サイト|視聴日|
|:--|:--|:--:|:--:|:--:|
|001|[画面操作･オブジェクトの操作･3Dカーソル](https://www.youtube.com/watch?v=du0ybLqScJk&index=1&list=PLmVkGpfcCZalGLfi3B5lx038GY1rNw2-L)|－|－|2018-04-20|
|002|[基本操作法（オブジェクトモード･編集モード）](https://www.youtube.com/watch?v=xgsTa-yiPHY)|－|－|2018-04-20|
|003|[機能紹介その①（基本動作）](https://www.youtube.com/watch?v=EHAgiNVKIPo)|[●](https://mubirou.github.io/Blender/introduction/blend/004_003.blend)|－|2018-04-20|
|004|[機能紹介その②（オブジェクトの色･アニメーション作成）](https://www.youtube.com/watch?v=KLm5B98zQV8)|[●](https://mubirou.github.io/Blender/introduction/blend/004_004.blend)|－|2018-04-21|
|005|[3Dテキストの作成](https://www.youtube.com/watch?v=3Jh_-HqSzmI)|[●](https://mubirou.github.io/Blender/introduction/blend/004_005.blend)|－|2018-04-21|
|006|[平面ライトの作り方](https://www.youtube.com/watch?v=dfoRfwacDSA)|－|－|2018-04-22|
|007|[綺麗なゴールドの設定](https://www.youtube.com/watch?v=DP1qJJkHmOQ)|[●](https://mubirou.github.io/Blender/introduction/blend/004_007.zip)|－|2018-04-22|
|008|[G･R･S + X･Y･Z + Ctrl](https://www.youtube.com/watch?v=RIR5p28CiZ4)|－|－|2018-04-22|
|009|[立方体からの変形（1･3･5 / E / B）](https://www.youtube.com/watch?v=wftv5exmsho)|[●](https://mubirou.github.io/Blender/introduction/blend/004_009.blend)|－|2018-04-23|
|010|[犬の作成①](https://www.youtube.com/watch?v=pkvMiEeJGro)･[②](https://www.youtube.com/watch?v=DUp9XAM42Cg)･[③](https://www.youtube.com/watch?v=sTdziqcgNnM)（A / B / Ctrl+R）|[●](https://mubirou.github.io/Blender/introduction/blend/004_010_01.blend)[●](https://mubirou.github.io/Blender/introduction/blend/004_010_02.blend)[●](https://mubirou.github.io/Blender/introduction/blend/004_010_03.blend)|－|2018-04-25|
|011|[UVマッピング](https://www.youtube.com/watch?v=IXXN3p8aCIM)|[●](https://mubirou.github.io/Blender/introduction/blend/004_011.zip)|－|2018-04-26|
|012|[ボーン（アーマチュア）の基本](https://www.youtube.com/watch?v=JULer0rGUBk)|[●](https://mubirou.github.io/Blender/introduction/blend/004_012.blend)|[●](https://yugalab.net/archives/2446)|2018-04-27|
|013|[ロゴアニメーション](https://www.youtube.com/watch?v=UBbkLTwx5WY)|[●](https://mubirou.github.io/Blender/introduction/blend/004_013.blend)|－|2018-04-28|
|014|[テキストに日本語を使う方法](https://www.youtube.com/watch?v=ISUJ8s_cHbM)|[●](https://mubirou.github.io/Blender/introduction/blend/004_014.blend)|－|2018-04-29|
|015|[20世紀フォックス風オープニング](https://www.youtube.com/watch?v=4iLOzG3eFh4)|[●](https://mubirou.github.io/Blender/introduction/blend/004_015.blend)|－|2018-04-29|
|016|[透明カップと布](https://www.youtube.com/watch?v=SSpoeL45oZ4)|[●](https://mubirou.github.io/Blender/introduction/blend/004_016.blend)|－|2018-04-30|
|017|[物理演算とオブジェクトの破壊](https://www.youtube.com/watch?v=fXMNR2InZqI)|[●](https://mubirou.github.io/Blender/introduction/blend/004_017.blend)|－|2018-05-02|
|018|[衝突破壊](https://www.youtube.com/watch?v=7wQ4bH499wU)|[●](https://mubirou.github.io/Blender/introduction/blend/004_018.blend)|－|2018-05-02|
|019|[基本ショートカット + Bool Tools](https://www.youtube.com/watch?v=g1E4N-osxQU)|－|－|2018-05-03|
|020|[カーブオブジェクト](https://www.youtube.com/watch?v=pYfRXz0tSBk)|[●](https://mubirou.github.io/Blender/introduction/blend/004_020.blend)|－|2018-05-04|
|021|[ワイングラス風](https://www.youtube.com/watch?v=rpdfeQRKSMg)|[●](https://mubirou.github.io/Blender/introduction/blend/004_021.blend)|－|2018-05-05|
|022|[カメラの設定](https://www.youtube.com/watch?v=ygrNtWcvoUg)|－|－|2018-05-06|
|023|[カメラのトラッキング](https://www.youtube.com/watch?v=Vu2Rtpuk6Aw)|[●](https://mubirou.github.io/Blender/introduction/blend/004_023.blend)|－|2018-05-06|
|024|[パスアニメーション](https://www.youtube.com/watch?v=4LpDGe-MpLE)|[●](https://mubirou.github.io/Blender/introduction/blend/004_024.blend)|－|2018-05-07|
|025|[流体シュミレーション](https://www.youtube.com/watch?v=inyfz4WsJt4)|[●](https://mubirou.github.io/Blender/introduction/blend/004_025.blend)|[●](https://blender-cg.net/fluid/)|2018-05-07|
|026|[スプリング（ばね）](https://www.youtube.com/watch?v=8UFcZBk6v9Y)|[●](https://mubirou.github.io/Blender/introduction/blend/004_026.blend)|－|2018-05-15|
|027|[歯車の作成とかみ合わせ](https://www.youtube.com/watch?v=iWRNMG9LAYY)|[●](https://mubirou.github.io/Blender/introduction/blend/004_027.blend)|[●](https://syoshinsya-3d.hatenablog.com/entry/2018/05/06/220800)|2018-05-21|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
作成日：2018年04月20日  
更新日：2018年05月21日


<a name="『CGイラストテクニック』"></a>
# <b>005 『無料ではじめるBlender CGイラストテクニック』</b>

頁数は [『無料ではじめるBlender CGイラストテクニック／大澤龍一著』](https://amzn.to/2HUNroF) のページです。  

|No.|内容|頁数|.blend|参考サイト|作成日|
|:--|:--|:--:|:--:|:--:|:--:|
|001|プリミティブでキャラクターを作る|029|[●](https://mubirou.github.io/Blender/introduction/blend/005_001.blend)|－|2018-05-07|
|002|プリミティブで木を作る|035|[●](https://mubirou.github.io/Blender/introduction/blend/005_002.blend)|－|2018-05-07|
|003|ガラスのコップ（一部色付き）を作る|041|[●](https://mubirou.github.io/Blender/introduction/blend/005_003.blend)|－|2018-05-08|
|004|細分割曲面で葉っぱを表現|051|[●](https://mubirou.github.io/Blender/introduction/blend/005_004.blend)|－|2018-05-08|
|005|帽子をかぶったサボテン君|052|[●](https://mubirou.github.io/Blender/introduction/blend/005_005.blend)|－|2018-05-08|
|006|イルカ（ミラー使用）|054|[●](https://mubirou.github.io/Blender/introduction/blend/005_006.blend)|－|2018-05-08|
|007|お城|055|[●](https://mubirou.github.io/Blender/introduction/blend/005_007.blend)|－|2018-05-09|
|008|さまざまな造形のアイデア|056|[●](https://mubirou.github.io/Blender/introduction/blend/005_008.blend)|－|2018-05-09|
|009|取っ手･ブーリアン|063|[●](https://mubirou.github.io/Blender/introduction/blend/005_009.blend)|－|2018-05-10|
|010|ナイフ･細分化･プロポーショナル編集|066|[●](https://mubirou.github.io/Blender/introduction/blend/005_010.blend)|－|2018-05-10|
|011|ドロー系ソフトからの読み込み / メッシュに変換|076 / 086|[●](https://mubirou.github.io/Blender/introduction/blend/005_011.zip)|－|2018-05-15|
|012|額縁（ベジェカーブと円カーブ）|084|[●](https://mubirou.github.io/Blender/introduction/blend/005_012.blend)|－|2018-05-15|
|013|ヘビ（Alt+C→カーブからメッシュに変換）|086|[●](https://mubirou.github.io/Blender/introduction/blend/005_013.blend)|－|2018-05-16|
|014|スクリュー|087|[●](https://mubirou.github.io/Blender/introduction/blend/005_014.blend)|－|2018-05-17|
|015|シャワーヘッド（ブーリアン）|088|[●](https://mubirou.github.io/Blender/introduction/blend/005_015.blend)|－|2018-05-17|
|016|スカルプトモデリング|095|[●](https://mubirou.github.io/Blender/introduction/blend/005_016.blend)|－|2018-05-17|
|017|配列複製（直線 / カーブ）|105|[●](https://mubirou.github.io/Blender/introduction/blend/005_017.blend)|[●](https://www.youtube.com/watch?v=-fzLGuckHh0)|2018-05-18|
|018|配列複製（格子）|107|[●](https://mubirou.github.io/Blender/introduction/blend/005_018.blend)|－|2018-05-18|
|019|配列複製（ビル）|108|[●](https://mubirou.github.io/Blender/introduction/blend/005_019.blend)|－|2018-05-18|
|020|パーティクルで大量複製配列の基本（植物）|109|[●](https://mubirou.github.io/Blender/introduction/blend/005_020.blend)|－|2018-05-20|
|021|パーティクルヘアー（髪の毛）|117|[●](https://mubirou.github.io/Blender/introduction/blend/005_021.blend)|－|2018-05-24|
|022|ソファーとぬいぐるみ|123|[●](https://mubirou.github.io/Blender/introduction/blend/005_022.blend)|－|2018-05-25|
|023|ひまわり（ウェイトペント / パーティクル→メッシュに変換）|135|[●](https://mubirou.github.io/Blender/introduction/blend/005_023.blend)|－|2018-05-29|
|024|やかん（別オブジェクトに分離）|141|[●](https://mubirou.github.io/Blender/introduction/blend/005_024.blend)|－|2018-05-29|
|025|マテリアル（光沢BSDF / ガラスBSDF）|148|[●](https://mubirou.github.io/Blender/introduction/blend/005_025.blend)|－|2018-05-29|
|026|マテリアルノード（ノードエディタ）|151|[●](https://mubirou.github.io/Blender/introduction/blend/005_026.blend)|－|2018-05-29|
|027|よく使う4種類のマテリアル（艶あり / 艶あり / 金属 / ガラス）|156|[●](https://mubirou.github.io/Blender/introduction/blend/005_027.blend)|－|2018-05-29|
|028|テクスチャ（フラット / ボックス / 球 / チューブ）|170|[●](https://mubirou.github.io/Blender/introduction/blend/005_028.zip)|[●](https://www.textures.com/)|2018-05-30|
|029|汚れた感じを足す（grunge / smudge）|178|[●](https://mubirou.github.io/Blender/introduction/blend/005_029.zip)|[●](https://www.textures.com/)|2018-05-30|
|030|オブジェクトの一部にマッピング（窓）|185|[●](https://mubirou.github.io/Blender/introduction/blend/005_030.zip)|[●](https://www.textures.com/)|2018-05-30|
|031|スマートUV投影 / テクスチャペイント|189|[●](https://mubirou.github.io/Blender/introduction/blend/005_031.blend)|－|2018-05-31|
|032|立方体のUV展開（シームを付ける）|199|[●](https://mubirou.github.io/Blender/introduction/blend/005_032.blend)|－|2018-05-31|
|033|有機曲面のUV展開（シームを付ける）|200|[●](https://mubirou.github.io/Blender/introduction/blend/005_033.zip)|－|2018-05-31|
|034|空の明るさ（大気テクスチャ）|214|[●](https://mubirou.github.io/Blender/introduction/blend/005_034.blend)|－|2018-05-31|
|035|美しいライティング（複数の光源）|216|[●](https://mubirou.github.io/Blender/introduction/blend/005_035.blend)|－|2018-05-31|
|036|カメラの設定（35フィルム 50mm F0.95 / 露出補正±10）|239|[●](https://mubirou.github.io/Blender/introduction/blend/005_036.blend)|－|2018-06-01|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
作成日：2018年05月07日  
更新日：2018年06月01日


<a name="ショートカットキー"></a>
# <b>006 ショートカットキー</b>

他のソフトウェアとの兼ね合いもありショートカットキーは多用しません。  
Ver.2.80 からアイコンを多用するようになりました。

|ショートカットキー|内容|DATE|
|:--|:--|:--:|
|[Del]|選択したオブジェクトを削除する|2018-05-24|
|[Shift]+[S]|3Dカーソルの位置を原点に移動する等|2018-05-24|
|[A]|全選択 / 2回連続で全選択解除|2019-05-08|
|[Z]|シェーディング選択（ワイヤーフレーム等）|2019-05-08|
|[S]|拡大･縮小|2018-05-25|
|[E]|押し出し|2019-05-08|
|[B]|矩形で範囲指定|2018-05-25|
|[C]|ドラッグで範囲指定|2018-05-25|
|[G]|自由移動（X･Y･Zの併用で方向限定）|2018-05-25|
|[P]|別オブジェクトに分離|2018-05-29|
|[Ctrl]+[J]|複数のオブジェクトを1つに統合|2018-05-30|
|[Ctrl]+[P]|２つのオブジェクトをペアレント（親）関係にする|2018-08-24|

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年05月24日  
更新日：2019年05月08日 Ver.2.80 対応


<a name="マウス操作"></a>
# <b>007 マウス操作</b>

Ver.2.80 からオブジェクトの選択が[左ボタン]に変更されました。

|マウス操作|内容|DATE|
|:--|:--|:--:|
|[左ボタン]|オブジェクトの選択|2019-05-08|
|[Shift]+[左ボタン]|オブジェクトの選択の追加 / 選択の解除|2019-05-08|
|[ホイール回転]|視点のズームアップ･ズームダウン（画面中央を基準）|2018-05-24|
|[中ボタン]+[ドラッグ]|視点の回転（選択したオブジェクトを基準）|2018-05-24|
|[Shift]+[中ボタン]+[ドラッグ]|視点の自由移動|2018-05-24|

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年05月24日  
更新日：2019年05月08日 Ver.2.80 対応


<a name="アドオン"></a>
# <b>008 アドオン</b>

* デフォルトで無効になっているアドオンがあります。
* [ファイル]-[ユーザー設定] で任意のアドオンを検索し [✔] → [ユーザー設定の保存] で有効化。
* [『無料ではじめるBlender CGイラストテクニック』](https://amzn.to/2HUNroF) 参考。

|アドオン名|内容|使用方法|.blend|
|:--|:--|:--|:--:|
|Extra Objects（Mesh）|ギヤ等の追加|[Shirt]-[A] から選択|[●](https://mubirou.github.io/Blender/introduction/blend/005_037_01.blend)|
|LoopTools|頂点を中心に円形に変形|[W] から選択|[●](https://mubirou.github.io/Blender/introduction/blend/005_037_02.blend)|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
作成日：2018年06月01日  


<a name="ルーティンワーク"></a>
# <b>009 ルーティンワーク</b>

* 画面を四分割表示した上で、カメラのアングルを常にエンプティの方向にすることで、容易に構図を調整できるようにします。

1. Blenderを起動。
1. 中央の立方体をマウスの [左ボタン] で選択し、[Del] で削除。
1. エリアの境界上で [左クリック] → [エリア分割]。  
    （[ビュー]-[エリア]-[四分割表示] しても良い）
1. [Shift]+[S] で [カーソル→ワールド原点] を選択（3Dカーソルの位置を原点に移動）。
1. [追加]-[エンプティ]-[十字] を選択。
1. [Camera] を選択してから [Shift] キーを押しながら [エンプティ] を選択。
1. [オブジェクト]-[トラック]-[トラック（コンストレイント）] を選択。  
    （ライト系と [エンプティ] も同様にトラッキングさせてもよい）
1. [Camera] や [エンプティ] の位置を任意で移動し、カメラの構図を調整。
 
実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年06月01日  
更新日：2019年05月08日 Ver.2.80 対応


<a name="『はじめてのBlender』"></a>
# <b>010 『はじめてのBlender（アニメーション編）』</b>

頁数は [『はじめてのBlender（アニメーション編）／山崎聡著』](https://amzn.to/2JiTi70) のページです。  

|No.|内容|頁数|.blend|参考サイト|作成日|
|:--|:--|:--:|:--:|:--:|:--:|
|003|アニメーション･チュートリアル①（モデリング･アーマチュア）|〜41|[●](https://mubirou.github.io/Blender/introduction/blend/010_001.blend)|－|2018-06-04|
|002|アニメーション･チュートリアル②（IK設定）|〜47|[●](https://mubirou.github.io/Blender/introduction/blend/010_002.blend)|－|2018-06-06|
|003|アニメーション･チュートリアル③（完成）|〜58|[●](https://mubirou.github.io/Blender/introduction/blend/010_003.blend)|－|2018-06-07|
|004|グラフエディタ（バウンス･ゴム状）|65|[●](https://mubirou.github.io/Blender/introduction/blend/010_004.blend)|[●](https://blender-cg.net/graph-editor/)|2018-06-08|
|005|パスアニメーション|78|[●](https://mubirou.github.io/Blender/introduction/blend/010_005.blend)|－|2018-06-11|
|006|列車（パスに追従コンストレイント）|82|[●](https://mubirou.github.io/Blender/introduction/blend/010_006.blend)|[●](https://www.youtube.com/watch?v=UnRaVTozxDk)|2018-06-12|
|007|モーフィング（シェイプキー･ドープシート）|86|[●](https://mubirou.github.io/Blender/introduction/blend/010_007.blend)|[●](https://blender-cg.net/shape-keys/)[●](https://blender-cg.net/dope-sheet/)|2018-06-12|
|008|スケルタル･アニメーション①（変形するMeshを作成）|92 / 35|[●](https://mubirou.github.io/Blender/introduction/blend/010_008.blend)|－|2018-06-13|
|009|スケルタル･アニメーション②（アーマチュア作成）|28〜41 / 92〜100|[●](https://mubirou.github.io/Blender/introduction/blend/010_009.blend)|－|2018-06-15|
|010|スケルタル･アニメーション③（ウェイト設定）|41〜44 / 101〜114|[●](https://mubirou.github.io/Blender/introduction/blend/010_010.blend)|－|2018-06-15|
|011|スケルタル･アニメーション④（IK･リギング）|45〜47 / 115〜127|[●](https://mubirou.github.io/Blender/introduction/blend/010_011.blend)|－|2018-06-15|
|012|スケルタル･アニメーション⑤（基本ループアニメ）|48〜55 / 128〜131|[●](https://mubirou.github.io/Blender/introduction/blend/010_012.blend)|－|2018-06-18|
|013|スケルタル･アニメーション⑥（パスのアニメ）|55〜58 / 132〜|[●](https://mubirou.github.io/Blender/introduction/blend/010_013.blend)|－|2018-06-18|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
作成日：2018年06月04日  
更新日：2018年06月18日


<a name="Unity用データ"></a>
# <b>011 Unity用データ</b>

### キャラクターの三角面（ポリゴン）の総数は5,000以下にする
    モンキー（細分化0）：968  
    モンキー（細分化1）：3,936  
    モンキー（細分化2）：15,744

### シェーディングは「スムーズ」にする
    Unity上でVerts（頂点数）の値が減り、FPSが高速になる

### マテリアル数をなるべく少なくする

### Unityにインポート可能なもの
* ボーン
* UV（Unity上でリンクし直す必要あり）

### システムに無いため持ち込めないデータ
* 各種ランプ
* カメラ

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
作成日：2018年06月19日  
更新日：2018年06月20日


<a name="『モデリングマスター』"></a>
# <b>012 『Blender 3DCG モデリング･マスター』</b>

頁数は [『Blender 3DCG モデリング･マスター／Benjamin著』](https://amzn.to/2A2595W) のページです。  

|No.|内容|頁数|.blend|参考サイト|作成日|
|:--|:--|:--:|:--:|:--:|:--:|
|001|星|64|[●](https://mubirou.github.io/Blender/introduction/blend/012_001.blend)|－|2018-07-24|
|002|スマートフォン|72|[●](https://mubirou.github.io/Blender/introduction/blend/012_002.blend)|－|2018-07-24|
|003|蛇腹|79|[●](https://mubirou.github.io/Blender/introduction/blend/012_003.blend)|－|2018-07-24|
|004|バネ|84|[●](https://mubirou.github.io/Blender/introduction/blend/012_004.blend)|－|2018-07-26|
|005|マグカップ|91|[●](https://mubirou.github.io/Blender/introduction/blend/012_005.blend)|－|2018-07-26|
|006|歯車|104|[●](https://mubirou.github.io/Blender/introduction/blend/012_006.blend)|－|2018-07-26|
|007|ネジ山|110|[●](https://mubirou.github.io/Blender/introduction/blend/012_007.blend)|－|2018-07-26|
|008|蝶|119|[●](https://mubirou.github.io/Blender/introduction/blend/012_008.blend)|－|2018-07-27|
|009|ペットボトル|131|[●](https://mubirou.github.io/Blender/introduction/blend/012_009.blend)|－|2018-07-27|
|010|テキストオブジェクト|146|[●](https://mubirou.github.io/Blender/introduction/blend/012_010.zip)|－|2018-07-27|
|011|配管|154|[●](https://mubirou.github.io/Blender/introduction/blend/012_011.blend)|－|2018-07-30|
|012|日本刀|168|[●](https://mubirou.github.io/Blender/introduction/blend/012_012.blend)|－|2018-08-06|
|013|タイヤ|204|[●](https://mubirou.github.io/Blender/introduction/blend/012_013.blend)|－|2018-08-06|
|014|動物キャラクター|220|[●](https://mubirou.github.io/Blender/introduction/blend/012_014.blend)|－|2018-08-06|
|015|スクーター|263|[●](https://mubirou.github.io/Blender/introduction/blend/012_015.blend)|－|2018-08-08|
|016|人間の頭部|308|[●](https://mubirou.github.io/Blender/introduction/blend/012_016.blend)|－|2018-08-09|

実行環境：Blender 2.79b、Ubuntu 16.04.4 LTS  
作成者：夢寐郎  
作成日：2018年07月24日  
更新日：2018年08月09日


<a name="『ブレンダーからはじめよう!』"></a>
# <b>013 『ブレンダーからはじめよう!』</b>

頁数は [『ブレンダーからはじめよう!／原田大輔著』](https://amzn.to/2vzog2t) のページです。  

|No.|内容|頁数|.blend|参考サイト|作成日|
|:--|:--|:--:|:--:|:--:|:--:|
|001|キャラクターが走る|41〜46|[●](https://mubirou.github.io/Blender/introduction/blend/013_001.blend)|－|2018-08-14|
|002|キャラクターをジャンプさせる|47〜56|[●](https://mubirou.github.io/Blender/introduction/blend/013_002.blend)|－|2018-08-16|
|003|キャラクターのモデリング|57〜78|[●](https://mubirou.github.io/Blender/introduction/blend/013_003.blend)|－|2018-08-16|
|004|アニメーションの修正|80〜85|[●](https://mubirou.github.io/Blender/introduction/blend/013_004.blend)|－|2018-08-17|
|005|アーマチュアで変形（頂点ウェイト）|86〜93|[●](https://mubirou.github.io/Blender/introduction/blend/013_005.blend)|－|2018-08-17|
|006|アーマチュアで変形（エンベロープ）|94〜95|[●](https://mubirou.github.io/Blender/introduction/blend/013_006.blend)|－|2018-08-17|
|007|人体モデルにアーマチュアを入れる|96〜105|[●](https://mubirou.github.io/Blender/introduction/blend/013_007.blend)|－|2018-08-21|
|008|人体モデルにIKをつける|106〜112|[●](https://mubirou.github.io/Blender/introduction/blend/013_008.blend)|－|2018-08-22|
|009|手を振るアニメーション|113〜117|[●](https://mubirou.github.io/Blender/introduction/blend/013_009.blend)|－|2018-08-22|
|010|歩行アニメーション|118〜122|[●](https://mubirou.github.io/Blender/introduction/blend/013_010.blend)|－|2018-08-23|
|011|アクションの作成（Stop / Walk / Run）|123〜136|[●](https://mubirou.github.io/Blender/introduction/blend/013_011.blend)|－|2018-08-24|
|012|ペアレント（親子関係 / 皿の上のボール）|137〜139|[●](https://mubirou.github.io/Blender/introduction/blend/013_012.blend)|－|2018-08-24|
|013|マテリアルの割り当て|143〜150|[●](https://mubirou.github.io/Blender/introduction/blend/013_013.blend)|－|2018-08-25|
|014|ランプ（天空光 / 照り返し）|151〜154|[●](https://mubirou.github.io/Blender/introduction/blend/013_014.blend)|－|2018-08-26|
|015|テクスチャで表情を作る（外部PNGファイル）|155〜165|[●](https://mubirou.github.io/Blender/introduction/blend/013_015.zip)|－|2018-08-27|

実行環境：Blender 2.79b、Ubuntu 18.0.4.1 LTS  
作成者：夢寐郎  
作成日：2018年08月10日  
更新日：2018年08月21日 Ubuntu 16.04.4 LTS を 18.0.4.1 LTS にアップデート  
更新日：2018年08月27日


<a name="テクニック･ヒント1"></a>
# <b>014 テクニック･ヒント1</b>

|No.|内容|作成日|
|:--|:--|:--:|
|001|[星型](#014_001)|2019-05-08|
|002|[ベベル･面取り](#014_002)|2019-05-08|
|003|[蛇腹](#014_003)|2019-05-08|
|004|[バネ](#014_004)|2019-05-08|
|005|[壁にパイプを結合](#014_005)|2019-05-09|
|006|[歯車](#014_006)|2019-05-10|
|007|[ネジ山](#014_007)|2019-05-10|
|008|[ハート型に掘る](#014_008)|2019-05-10|
|009|[下絵の利用](#014_009)|2019-05-10|
|010|[テキストオブジェクト](#014_010)|2019-05-10|
|011|[パイプ](#014_011)|2019-05-11|
|012|[UFO（エッジのシャープ化）](#014_012)|2019-05-11|


<a name="014_001"></a>
### 001 星型

![014_001](https://mubirou.github.io/Blender/introduction/jpg/014_001.jpg)

1. [追加]-[メッシュ]-[サークル]
1. 上記を操作したウィンドウの画面左下にある[円を追加]を開き調整
    * 頂点：10（五角星の場合）←**偶数にする**
    * フィルタタイプ：**三角の扇形**
1. [オブジェクトモード]→[編集モード]にする
1. 外周のポイントを１つおきに選択
1. [拡大･縮小](#ショートカットキー)で星型にする  
    （面を張る場合は、頂点群を選択→[面]-[フィル]を選択）

    ※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_001.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月17日  
更新日：2019年05月08日 Ver.2.80 対応


<a name="014_002"></a>
### 002 ベベル･面取り

![014_002](https://mubirou.github.io/Blender/introduction/jpg/014_002.jpg)

1. [追加]-[メッシュ]-[立方体]を選択
1. 立方体を選択し[編集モード]にする
1. [辺選択]で任意の線を選択（複数可）
1. [辺]-[辺をベベル]を選択
1. マウスのドラッグでベベルを作成（挙動がわかりにくい）
1. 上記を操作したウィンドウの左下にある[べべル]を開き調整（例）
    * 幅：0.5m（0〜∞）
    * セグメント：5（値を大きくすると滑らかになる）
    * 側面：0.500（0.000〜1.000）

    ※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_002.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月17日  
更新日：2019年05月08日 Ver.2.80 対応


<a name="014_003"></a>
### 003 蛇腹

![014_003](https://mubirou.github.io/Blender/introduction/jpg/014_003.jpg)

1. [追加]-[メッシュ]-[円柱]
1.  上記を操作したウィンドウの左下にある[円柱を追加]を開き調整（例）
    * 深度：3m
    * ふたのフィルタタイプ：なし
1. [オブジェクトモード]→[編集モード]にする
1. 左側のアイコン群の中から[LoopCut]を選択
1. ループカットしたい面でとりあえずクリック（2.7xと異なる）
1. 上記を操作したウィンドウの左下にある[ループカットとスライド]を開き調整（例）  
    * 分割数：17 ←奇数にする
1. 以下の状態にしてから次の作業を行う  
    * 左側のアイコン群の一番上「SelectBox」を選択
    * 「フロント」「平行投影」にする
    * 「シーン全体を透過表示にします」アイコンを選択
1. [矩形で範囲指定](#ショートカットキー)で1本おきにループ状に選択
1. 左側のアイコン群の中から「Scale」を選択
1. 3Dマニュピレーターの中央の白い輪をドラッグして縮小（要注意）  
    （Shiftキーを押しながら行うと微調整可能）
1. 上記を操作したウィンドウの左下にある[拡大縮小]を開き調整
        * X：0.800（任意）
        * Y：0.800（任意）
        * Z：1.000 ←重要

    ※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_003.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月18日  
更新日：2019年05月08日 Ver.2.80 対応


<a name="014_004"></a>
### 004 バネ

![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_2.jpg)

1. [追加]-[メッシュ]-[サークル]
1. 上記を操作したウィンドウの左下にある[円を追加]を開き調整
    * 頂点：12
    * 半径：0.2m
    * 回転（X）：90°
1. [オブジェクト]-[適用]-[回転] ←回転した状態をデフォルトとして適用 ←重要  
    （[オブジェクト]-[トランスフォーム]-[回転]-[X]の値が90°→0°になる）
1. [オブジェクトモード]→[編集モード]にする
1. 円をX軸マイナス方向に移動（-0.5m程度）
1. [編集モード]→[オブジェクトモード]に変更
1. (0,0,0)の位置に[追加]-[エンプティ]-[十字]で空のオブジェクトを作成
1. 円のオブジェクトを選択して[オブジェクトモード]→[編集モード]に変更
1. 円を選択した状態で、右側のスパナ
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    タブを選択→[モディファイアーを追加]-[生成]-[スクリュー]を選択し各種設定  
    * 軸オブジェクト：エンプティ（上記で作成）
    * スクリュー：0.5m
    * 反復：5
1. 再び[編集モード]→[オブジェクトモード]に変更
1. ①円と②エンプティを選択
1. [オブジェクト]-[ペアレント]-[オブジェクト]-[オブジェクト（トランスフォーム維持）] を選択

    ※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_004.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月19日  
更新日：2019年05月08日 Ver.2.80 対応


<a name="014_005"></a>
### 005 壁にパイプを結合

![014_005_1](https://mubirou.github.io/Blender/introduction/jpg/014_005_1.jpg)

#### ◆平面を作成
1. [追加]-[メッシュ]-[平面]
1. 上記を操作したウィンドウの左下にある[平面を追加]を開き調整
    * 回転（X）：90°

#### ◆パイプを作成
1. [追加]-[メッシュ]-[円柱]
1. 上記を操作したウィンドウの左下にある[円柱を追加]を開き調整
    * 頂点：8
    * 半径：0.2m
    * 位置（Y）：-1.1m
    * 回転（X）：90°

### ◆平面とパイプを１つのオブジェクトにする
1. 上記の平面と円柱を両方選択
1. [オブエジェクト]-[結合]
1. [オブジェクトモード]→[編集モード]にする

    ![014_005_2](https://mubirou.github.io/Blender/introduction/jpg/014_005_2.jpg)

#### ◆穴をあける
1. 左側のアイコン群の中から[LoopCut]を選択
1. ループカットしたい面で（横方向）とりあえずクリック（2.7xと異なる）
1. 上記を操作したウィンドウの左下にある[ループカットとスライド]を開き調整（例）  
    * 分割数：2
1. 縦方向にもも上記と同様の方法を行う
1. 更に縦横中央に1本ずつ十字にカット
1. Scale機能を使ってサイズを調整
1. [面選択]を使って穴をあける
1. [頂点選択]を使って穴を形をパイプに近づける（図はフロント･並行投影）

    ![014_005_3](https://mubirou.github.io/Blender/introduction/jpg/014_005_3.jpg)

#### ◆穴の部分を結合
1. [頂点選択]を使って結合したいところ全て選択
1. [辺]-[辺ループのブリッジ]で結合 ←1つ1つ面を作るより早い

    ![014_005_4](https://mubirou.github.io/Blender/introduction/jpg/014_005_4.jpg)

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_005.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月19日  
更新日：2019年05月09日 Ver.2.80 対応


<a name="014_006"></a>
### 006 歯車

![014_006_1](https://mubirou.github.io/Blender/introduction/jpg/014_006_1.jpg)

#### ◆歯車を作成
1. [追加]-[メッシュ]-[サークル]
1. 上記を操作したウィンドウの左下にある[円を追加]を開き調整
    * 頂点：32 ←偶数にする
    * フィルタイプ：なし
1. [オブジェクトモード]→[編集モード]にする
1. 外周のポイントを１つおきに選択
1. [拡大･縮小](#ショートカットキー)で星型にする
1. 全てを選択した状態で[メッシュ]-[複製]→そのまま[右ボタンで確定
1. 左側のアイコン群の中から[Rotate]を選び少し回転  
    ![014_006_2](https://mubirou.github.io/Blender/introduction/jpg/014_006_2.jpg)
1. 上記を操作したウィンドウの左下にある[回転]を開き微調整
1. 全てを選択した状態で[メッシュ]-[削除]-[辺と面のみ]を選択（頂点のみ残る）
1. 全てを選択した状態で[頂点]-[頂点からの新規辺/面]
1. [面選択]で面を選択して[押し出し](#ショートカットキー)（厚みを付ける）

#### ◆穴をあける（ブーリアン）
1. [編集モード]→[オブジェクトモード]にする
1. [追加]-[メッシュ]-[円柱]で穴をあけるためのオブジェクトを作成（後に削除）
1. [拡大･縮小](#ショートカットキー)で穴のサイズを決める  
    ![014_006_3](https://mubirou.github.io/Blender/introduction/jpg/014_006_3.jpg)
1. 上記の"歯車のみを選択"した状態でスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[ブーリアン]を選択し各種設定
    * 演算：差分
    * オブジェクト：円柱 ←上記で作成したもの
1. [シーンコレクション]のツリー上の円柱を見えなくする

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_006.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月20日  
更新日：2019年05月10日 Ver.2.80 対応


<a name="014_007"></a>
### 007 ネジ山

![014_007_1](https://mubirou.github.io/Blender/introduction/jpg/014_007_1.jpg)

#### ◆ネジの頭部を作成
1. [追加]-[メッシュ]-[UV球]
1. 上記を操作したウィンドウの左下にある[UV球を追加]を開き調整
    * セグメント：16
    * リング：24
1. [編集モード]で（重要）上下につぶし半分を削除（下部は面にする）

#### ◆十字の凹み部分を作成
1. [オブジェクトモード]で新たに[立方体]を整形
1. [オブジェクト]-[オブジェクトの複製]→90°回転して十字型にする  
    （Ver.2.8では十字に「統合」するとダメっぽい）  
    ![014_007_2](https://mubirou.github.io/Blender/introduction/jpg/014_007_2.jpg)

#### ◆ネジを凹ます
1. [オブジェクトモード]でネジの頭部のみ選択
1. スパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[ブーリアン]を選択し各種設定
    * 演算：差分
    * オブジェクト：立方体 ←上記で作成した十字型のうち縦横どちらか
1. [アウトライナー]のツリー上の立方体（十字のオブジェクト）を見えなくする
1. 同様に十字型の残り1つをブーリアンの対象オブジェクトとする

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_007.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月21日  
更新日：2019年05月10日 Ver.2.80 対応


<a name="014_008"></a>
### 008 ハート型に掘る

![014_008_1](https://mubirou.github.io/Blender/introduction/jpg/014_008_1.jpg)

1. [追加]-[メッシュ]-[UV球]
1. [オブジェクトモード]→[編集モード]にする
1. [ビュー]-[視点]-[前]にして[並行投影]にする
1. [選択]-[なし]で選択を全て解除
1. 左側のアイコン群から[Knife]アイコンを選択
1. 左クリックを繰返しながらハート型を作成
1. 終点（始点と同じ）で[Enter]キーを押す ←わかりにくい  
    ![014_008_2](https://mubirou.github.io/Blender/introduction/jpg/014_008_2.jpg)
1. [面選択]でハート全体を選択
1. [押し出し](#ショートカットキー)で凹ます
1. 凹みのメッシュを平坦にしたい場合は[拡大縮小]で平らにする（次の方法を使うと便利）
    * [ビュー]-[視点]-[右]する
    * [ワイヤーフレーム]にする
    * [シーン全体を透過表示します]ボタンを選択
    * 画面左側のアイコン群から[拡大縮小]を選択し調整
        * X: **1.000**
        * Y: **0.000**
        * Z: **1.000**

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_008.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月21日  
更新日：2019年05月10日 Ver.2.80 対応


<a name="014_009"></a>
### 009 下絵の利用

![014_009_1](https://mubirou.github.io/Blender/introduction/jpg/014_009_1.jpg)

#### ◆下絵の用意
1. 方眼罫ノートなどを利用して「正面」と「右横」から見たイラストを作成
1. "シンプルスキャン"を使ってスキャニング（デスクトップ上に.pngファイルで保存）  
    ![014_009_2](https://mubirou.github.io/Blender/introduction/jpg/014_009_2.jpg)

#### ◆下絵の読込み
1. Blenderで3Dビューを3つ（①フロント･並行投影 ②ライト･並行投影 ③ユーザー･並行投影）用意する
1. "①フロント･並行投影" の3Dビューを選択
1. デスクトップ上から"①フロント･並行投影"の領域にドラッグ＆ドロップ
1. 画面右側のアイコン群に登場した[オブジェクトデータ]アイコン（画像のマーク）を選択し調整  
    * サイズ：任意（初期値5m）←ここで確定しておく
    * アルファを使用：✔
    * 透過：0.2（0.000〜1.000）
    * 側面：両方（初期値）
1. [追加]-[エンプティ]-[画像]を選択
1. 上記を操作したウィンドウの左下にある[エンプティ追加]を開き調整
    * 回転X：90°
1. フロントから見て中心になるように[Move]アイコンを使って移動
1. 下絵を選択した状態で[オブジェクト]-[オブジェクトを複製]→[右クリック]で確定
1. 画面左側にある[Rotate]アイコンを選択し少し回転
1. 上記を操作したウィンドウの左下にある[回転]を開き調整
    * 角度：-90°
    * 座標軸：Z  
    ![014_009_3](https://mubirou.github.io/Blender/introduction/jpg/014_009_3.jpg)

#### ◆モデリング
1. 下絵を参考にモデリング
1. モデリング途中の[編集モード]でスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モデファイアーを014_009_3追加]-[ミラー]を選択し各種設定
    * 軸：X
    * クリッピング：✔ ←鏡像との境界からメッシュがはみ出ないようになる

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/zip/014_009.zip)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月26日  
更新日：2019年05月10日 Ver.2.80 対応


<a name="014_010"></a>
### 010 テキストオブジェクト

![014_010](https://mubirou.github.io/Blender/introduction/jpg/014_010.jpg)

#### フォントの用意
1. https://www.1001freefonts.com/ から任意のフォントを選択
1. ダウンロードしたら解凍（**.TTF**ファイルのみ必要 / インストールは不要）

#### テキストオブジェクトの作成
1. [追加]-[テキスト]を選択
1. [オブジェクトモード]→[編集モード]に変更
1. 表示文字を "Text" から任意の文字に変更
1. 右側のアイコンタブの中からの「**a**」アイコンを選択
1. [フォント]-[標準]のフォルダーアイコンから上記の **.TTF** ファイルを指定
1. 引き続き各種設定
    * [シェイプ]-[プレビュー解像度U]：12（1〜64）
    * [ジオメトリ]-[押し出し]：0.15m
    * [ベベル]-[深度]：任意

* [オブジェクトモード]に変更後、[オブジェクト]-[変換]-[テキストからカーブ]や[テキストからメッシュ]で編集も可能  
* カーブに沿って文字を並べることも可能（要調査）

* 参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/zip/014_010.zip)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月26日  
更新日：2019年05月10日 Ver.2.80 対応


<a name="014_011"></a>
### 011 パイプ

![014_011_1](https://mubirou.github.io/Blender/introduction/jpg/014_011_1.jpg)

#### ◆カーブの作成（いきなり[追加]-[カーブ]で作成してもよい）
1. [円]や[平面]などを編集してパイプとなる[頂点]と[辺]で構成されるオブジェクトを以下の機能を使うなどして作成  
    * [オブジェクト]-[統合]
    * [頂点]-[頂点からの新規辺]
    * [押し出し](#ショートカットキー) ←頂点の押し出し
    ![014_011_2](https://mubirou.github.io/Blender/introduction/jpg/014_011_2.jpg)
1. [編集モード]→[オブジェクトモード]に変更
1. [オブジェクト]+[変換]で[メッシュ/テキストからカーブ]で "カーブ" に変換

#### ◆カーブをパイプ形状にする
1. [オブジェクトモード]で[プロパティエディタ]-
![014_011_3](https://mubirou.github.io/Blender/introduction/jpg/014_011_3.jpg)
で各種設定
    * [シェイプ]-[フィルモード]：フル（初期値：ハーフ）
    * [ジオメトリ]-[ベベル]-[深度]：0.2m
    * [ジオメトリ]-[ベベル]-[解像度]：4（0〜32）

#### ◆パイプに厚みを付ける（オプション）
1. [オブジェクトモード]で、[オブジェクト]+[変換]→[カーブからメッシュ]に変更
1. [編集モード]にして、右側のスパナ
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    タブを選択→[モディファイアーを追加]-[生成]-[ソリッド化]を選択し設定  
        * 幅：0.05m

#### ◆途中の太さを変更する（オプション）
1. [編集モード]で、左側のアイコン群から[LoopCut]を選択
1. ループカットしたい面でとりあえずクリック（2.7xと異なる）
1. 上記を操作したウィンドウの左下にある[ループカットとスライド]を開き調整（例）  
    * 分割数：2  e 
    ![014_011_4](https://mubirou.github.io/Blender/introduction/jpg/014_011_4.jpg)
1. 太くしたい部分を選択した状態で（面選択）、[面]-[法線に沿って面を押し出し]で操作

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_011.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2018年12月27日  
更新日：2019年05月11日 Ver.2.80 対応


<a name="014_012"></a>
### 012 UFO（エッジのシャープ化）

![014_012_1](https://mubirou.github.io/Blender/introduction/jpg/014_012_1.jpg)

#### ◆UFOの制作
1. [追加]-[メッシュ]-[円]を選択後調整
    * 頂点：24
    * フィルタイプ：三角の扇形
1. 視点をトップにして、[Scale]アイコンを使って拡大
1. 画面右側のアイコン群に登場した[拡大縮小]を開き調整
    * X,Y,Z 共に1.600
1. [編集モード]にして（視点はフロント）、[押し出し](#ショートカットキー)で厚みをつける（0.2m程度）
1. [オブジェクトモード]にして、[追加]-[メッシュ]-[UV球]
1. 画面右側のアイコン群に登場した[UV球を追加]を開き調整
    * セグメント：12
    * リング：12
1. 円の厚み分弱、UV球を上に移動
1. UV球を選択し[編集モード]にして半分削除
1. 上記の下部に小さなUV球を4つ追加  
    ![014_012_2](https://mubirou.github.io/Blender/introduction/jpg/014_012_2.jpg)
1. UFOの全てのパーツを選択した状態で[オブジェクト]-[統合]

#### ◆滑らかにする
1. [オブジェクトモード]状態で、右側のスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[細分割曲面]→各種設定  
        * ビュー：2（初期値1）
        * レンダー：2（初期値2）
1. [オブジェクト]-[スムーズシェード]を選択  
    ![014_012_3](https://mubirou.github.io/Blender/introduction/jpg/014_012_3.jpg)

#### ◆一部をシャープなエッジにする
1. [編集モード]に変更
1. [全選択解除](#ショートカットキー)する
1. [辺選択]でシャープなエッジにしたい辺を選択（Ctrl+マウス右ボタン）  
1. [N]キーで[トランスフォーム]を表示し調整
    * 辺データ：平均クリース：1.00  
    ![014_012_4](https://mubirou.github.io/Blender/introduction/jpg/014_012_4.jpg)

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/014_012.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2019年01月04日  
更新日：2019年05月11日 Ver.2.80 対応


<a name="テクニック･ヒント2"></a>
# <b>015 テクニック･ヒント2</b>

|No.|内容|作成日|
|:--|:--|:--:|
|001|[ブロック（エッジの超シャープ化と配列複製）](#015_001)|2019-05-12|
|002|[ワイングラス](#015_002)|2019-01-08|
|003|[額縁](#015_003)|2019-01-08|
|004|[窓（正確なUVマッピング）](#015_004)|2019-01-09|
|005|[サイコロ](#015_005)|2019-01-09|


<a name="015_001"></a>
### 001 ブロック（エッジの超シャープ化と配列複製）

![015_001](https://mubirou.github.io/Blender/introduction/jpg/015_001_1.jpg)

#### ◆ブロックのパーツを作成
1. [追加]-[メッシュ]-[立方体]で立方体を1つ作成
1. [編集モード]に変更
1. 上の面だけ選択して[面]-[面を差し込む]  
    ![015_001_2](https://mubirou.github.io/Blender/introduction/jpg/015_001_2.jpg)
1. 引き続き[面]-[面を押し出し]
1. [オブジェクトモード]に変更
1. 左側のアイコン群の中からスパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)タブを選択
1. [モディファイアーを追加]-[細分割曲面]→各種設定  
        * ビュー：2（初期値：1）
        * レンダー：2
1. [オブジェクト]-[スムーズシェード]を選択  

#### ◆エッジの超シャープ化
1. [編集モード]に戻す
1. エッジをシャープにしたい辺を選択（Shift+右クリック）  
    ![015_001_3](https://mubirou.github.io/Blender/introduction/jpg/015_001_3.jpg)
1. [N]キーで[トランスフォーム]を表示し調整
    * 辺データ：平均クリース：1.00 
1. シャープさが不足している場合、[LoopCut]を使って、分割線をシャープにしたいエッジ部分で重ねます  
    ![015_001_4](https://mubirou.github.io/Blender/introduction/jpg/015_001_4.jpg)

#### ◆配列複製
1. [編集モード]のまま、スパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[配列]→各種設定  
        * 数：2  
        * オフセット（倍率）  
            * **1.000** ←X軸方向  
            * 0.000  
            * 0.000  
1. もう一度[配列複製]→各種設定  
        * 数：3  
        * オフセット（倍率）  
            * 0.000  
            * **1.000** ←Y軸方向  
            * 0.000  

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/015_001.blend)

実行環境：Blender 2.80 Beta、Ubuntu 18.04.2 LTS  
作成者：夢寐郎  
作成日：2019年01月06日  
更新日：2019年05月12日 Ver.2.80 対応


<a name="015_002"></a>
### 002 ワイングラス

![015_002_1](https://mubirou.github.io/Blender/introduction/jpg/015_002_1.jpg)

#### ◆ドロー系ソフトからの読み込み
1. [Inkscape](https://github.com/mubirou/Inkscape)などでワインの断面を[作成](https://mubirou.github.io/Blender/introduction/svg/wineglass.svg)（プレーンSVGファイル）
1. Blender上で[ファイル]-[インポート]-[ScalableVectorGraphics（.svg）]から上記の.svgファイルをインポート
1. [ビュー]-[プロパティ]-[トランスフォーム]-[回転]の調整  
    * X：**90**°
    * Y：0°
    * Z：0°

#### ◆カーブの回転体を作る
1. [編集モード]に変更
1. Z軸がワインの中心軸になるように移動  
    ![015_002_2](https://mubirou.github.io/Blender/introduction/jpg/015_002_2.jpg)

1. スパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[追加]-[スクリュー]→各種設定  
        * 座標軸：Y  

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/015_002.blend)

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
作成日：2019年01月08日


<a name="015_003"></a>
### 003 額縁

![015_003](https://mubirou.github.io/Blender/introduction/jpg/015_003.jpg)

#### ◆ドロー系ソフトからの読み込み
1. [Inkscape](https://github.com/mubirou/Inkscape)などで額縁の断面を[作成](https://mubirou.github.io/Blender/introduction/svg/frameDesign.svg)（プレーンSVGファイル）
1. 同様に額縁のサイズとなる矩形を[作成](https://mubirou.github.io/Blender/introduction/svg/frameSize.svg)（プレーンSVGファイル）
1. Blender上で[ファイル]-[インポート]-[ScalableVectorGraphics（.svg）]から上記の.svgファイルをインポート
1. [編集モード]に変更して位置やサイズを調整
1. [オブジェクトモード]に変更して[プロパティエディタ]-
![014_011_3](https://mubirou.github.io/Blender/introduction/jpg/014_011_3.jpg)
で[ベベルオブジェクト]を上記の額縁の断面のオブジェクトにする

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/015_003.blend)

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
作成日：2019年01月08日


<a name="015_004"></a>
### 004 窓（正確なUVマッピング）

![015_004_1](https://mubirou.github.io/Blender/introduction/jpg/015_004_1.jpg)

#### テクスチャの用意
1. テクスチャを用意（[window.png](https://mubirou.github.io/Blender/introduction/png/window.png)）  
    ※テクスチャは[textures.com](https://www.textures.com/)を利用するとよいでしょう
1. [作成]-[立方体]で立方体を作成
1. [編集モード]に変更して[ツール]-[ループカットとスライド]で窓の位置に合わせて分割
1. 何れかの3Dビュー画面左下アイコンから[エディター]タイプを[UV画像エディター]に変更
1. テクスチャを貼りたい面を選択
1. [シェーディング/UV]タブ-[UV]-[展開]-[スマートUV投影]→[OK]を選択
1. [UV画像エディター]画面の[開く]から、上記の.pngファイルを選択  
    ![015_004_2](https://mubirou.github.io/Blender/introduction/jpg/015_004_2.jpg)  
    ※この画面で範囲の変更や角度を調整します
1. [編集モード]で、テクスチャを貼りたい面を選択している事を確認
1. ![015_004_5](https://mubirou.github.io/Blender/introduction/jpg/015_004_5.jpg)
    アイコンを押し→[新規]
1. ![015_004_3](https://mubirou.github.io/Blender/introduction/jpg/015_004_3.jpg)
    アイコンを選択→[新規]→[画像]→
    ![015_004_4](https://mubirou.github.io/Blender/introduction/jpg/015_004_4.jpg)
    アイコンから上記で登録済みの.pngファイルを選択  
    ![015_004_6](https://mubirou.github.io/Blender/introduction/jpg/015_004_6.jpg)
1. 引き続き各種設定  
    * [画像のマッピング]-[延長]：クリップ
    * [マッピング]-[座標]：UV  
1. 他の面を選択
1. ![015_004_5](https://mubirou.github.io/Blender/introduction/jpg/015_004_5.jpg)
    アイコンを押し→[+]→[新規]→[ディフューズ]の色（任意）を変更→[割り当て]
1. [3Dビューのシェーディング]を[ソリッド]→[マテリアル]に変更するなどして、テクスチャのマッピング具合を確認

※Unityで利用する場合は.fbxファイルでエクスポートし、テクスチャ（.png）と一緒に（相対的階層を維持したまま）Unityプロジェクトの[Assets]フォルダに保存して下さい

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/zip/015_004.zip)

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
作成日：2019年01月09日


<a name="015_005"></a>
### 005 サイコロ

![015_005_1](https://mubirou.github.io/Blender/introduction/jpg/015_005_1.jpg) 

1. [展開図](https://mubirou.github.io/Blender/introduction/png/dice.png)を用意
1. [作成]-[立方体]で作成
1. [編集モード]に変更
1. 上の展開図を参考に、立方体の上がサイコロの1になるように、辺選択で切れ目（シーム）を選択  
    ![015_005_2](https://mubirou.github.io/Blender/introduction/jpg/015_005_2.jpg)
1. [シェーディング/UV]タブを開く
1. 何れかの3Dビュー画面の[エディター]タイプを[UV画像エディター]に変更
1. [面選択]で立方体の全ての面を選択
1. [UV]-[シームを付ける]→[展開]を選択  
    ![015_005_3](https://mubirou.github.io/Blender/introduction/jpg/015_005_3.jpg)
1. [UV画像エディター]画面の[開く]から、上記の展開図（.pngファイル）を選択
1. パスの全てを選択後、[ツール]-[UV整列]-[90度回転]や、ポイントを選択して移動するなどして、テクスチャと展開図を合わせる
1. [編集モード]で、テクスチャを貼りたい面を選択している事を確認
1. ![015_004_5](https://mubirou.github.io/Blender/introduction/jpg/015_004_5.jpg)
    アイコンを押し→[新規]
1. ![015_004_3](https://mubirou.github.io/Blender/introduction/jpg/015_004_3.jpg)
    アイコンを選択→[新規]→[画像]→
    ![015_004_4](https://mubirou.github.io/Blender/introduction/jpg/015_004_4.jpg)
    アイコンから上記で登録済みの展開図（.pngファイル）を選択  
    ![015_004_6](https://mubirou.github.io/Blender/introduction/jpg/015_004_6.jpg)
1. 引き続き各種設定  
    * [画像のマッピング]-[延長]：クリップ
    * [マッピング]-[座標]：UV

※Unityで利用する場合は.fbxファイルの他、テクスチャ（.png）も必要です

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/zip/015_005.zip)

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
更新日：2019年01月09日


<a name="テクニック･ヒント3"></a>
# <b>016 テクニック･ヒント3</b>

|No.|内容|作成日|
|:--|:--|:--:|
|001|[スタンドライト（モデリング〜アーマチュアの設定）](#016_001)|2019-01-16|
|002|[スタンドライト（ポージング〜FBX出力）](#016_002)|2019-01-17|
|003|[Unity Humanoid用モデリング](#016_003)|2019-01-22|


<a name="016_001"></a>
### 001 スタンドライト（モデリング〜アーマチュアの設定）

![016_001](https://mubirou.github.io/Blender/introduction/jpg/016_001_1.jpg)

#### ◆モデリング
1. 円柱から、[ループカット][押し出し][クリース:1.00]などを使ってモデリング  
    ![016_001_2](https://mubirou.github.io/Blender/introduction/jpg/016_001_2.jpg)  
    ※パーツ毎に作成した場合は[オブジェクト]-[統合]で1つのオブジェクトにする  
    ※ウェイト調整がしやすいように広げた状態でモデリングする 
1. [オブジェクトモード]でスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[追加]-[細分割曲面]→各種設定  
        * ビュー：2  
        * レンダー：2
1. [ツール]-[シェーディング]-[スムーズ]を選択   

※ここまでの参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/016_001_1.blend)

#### ◆アーマチュアの作成
1. 上記のオブジェクトを選択し[オブジェクトモード]にする
1. [ワイヤーフレーム表示](#ショートカットキー)にする
1. [追加]-[アーマチュア]-[単一ボーン]を選択  
1. ボーンの関節をモデルの関節に合わせます ←重要  
    ![016_001_3](https://mubirou.github.io/Blender/introduction/jpg/016_001_3.jpg)  
1. プロパティエディタの![016_001_4](https://mubirou.github.io/Blender/introduction/jpg/016_001_4.jpg)
    アイコンを選択→[表示]→[レントゲン]を✔する（ワイヤーフレームでなくてもボーンが見えるようになります）  
    ![016_001_5](https://mubirou.github.io/Blender/introduction/jpg/016_001_5.jpg)
1. 上記で作成した[アーマチュア]を選択した状態で[編集モード]にする
1. ボーンの先端（丸い部分）を選択→[押し出し](#ショートカットキー)→繰り返す  
    ※土台部分にもボーンを伸ばします（Unity上での不具合回避のため）←重要
1. 各ボーンの関節をモデルの関節に合わせます ←重要  
    ![016_001_6](https://mubirou.github.io/Blender/introduction/jpg/016_001_6.jpg)
1. オブジェクトのメッシュ化
    1. [オブジェクトモード]で上記のオブジェクト（スタンドライト）を選択
    1. [Alt]+[C]でメッシュに変換  
    1. [編集モード]にして[ツール]-[削除]-[重複頂点を削除]で無駄な頂点を削除しておきます（オプション）
1. オブジェクトとアーマチュアの関連付け
    1. [オブジェクトモード]で①オブジェクト（スタンドライト）→②アーマチュアの順番に[Shift]キーを押しながら選択
    1. [オブジェクト]-[親]-[自動のウェイトで]-[自動のウェイトで]を選択  
    ※親子関係を解除する場合は、オブジェクトとアーマチュアを選択した状態で、[オブジェクト]-[親]-[親子関係をクリア]を選択

#### ◆ウェイトの調整（オプション）
1. 変形のテスト
    1. [オブジェクトモード]でアーマチュアを選択→[ポーズモード]に変更
    1. 任意のボーンを選択し[回転](#ショートカットキー)等で動かしてみる
    1. 不具合を確認（ソケットカバー部分に歪みが生じている）  
        ![016_001_7](https://mubirou.github.io/Blender/introduction/jpg/016_001_7.jpg)
    1. 全てのボーンを選択→[ポーズ]→[トランスフォームをクリア]→[すべて]でポーズを元に戻す
1. アーマチュア＝[ポーズモード]の状態で、オブジェクト（スタンドライト）を[ウェイトペイントモード]に変更
1. マウスの右ボタンでボーンを選択→[ツール]-[ブラシ]で影響する範囲を修正（以下注意点）  
    * [ツール]-[ブラシ]を次の通りに設定  
        * ウェイト：1.000 ←真っ赤にする
        * 強さ：1.000
    * マスクを利用する＝ペンマスク用のアイコン
    ![016_001_9](https://mubirou.github.io/Blender/introduction/jpg/016_001_9.jpg)で選択
    * [ワイヤーフレーム](#ショートカットキー)で作業するとわかりやすい  
    ![016_001_8](https://mubirou.github.io/Blender/introduction/jpg/016_001_8.jpg)  

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/016_001_2.blend)

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
作成日：2019年01月17日


<a name="016_002"></a>
### 002 スタンドライト（ポージング〜FBX出力）

![016_002_1](https://mubirou.github.io/Blender/introduction/jpg/016_002_1.jpg)

#### ◆準備
1. アーマチュアを関連付けたオブジェクト（.blendファイル）を用意する  
    （ここでは上記の[スタンドライト](#016_001)を使用します）
1. 任意のエリアを[3Dビュー]→[ドープシート]に変更  
    ![016_002_2](https://mubirou.github.io/Blender/introduction/jpg/016_002_2.jpg)
1. 引き続き[ドープシート]→[アクション]に変更  
    ![016_002_3](https://mubirou.github.io/Blender/introduction/jpg/016_002_3.jpg)
1. [新規]ボタンを選択し、"Action"→"**Normal**"に変更 ←1つめのポーズ名
1. 引き続き[**+**]ボタンを選択し、"Normal.001"→"**Down**"に変更 ←2つめのポーズ名
1. 引き続き[**+**]ボタンを選択し、"Down.001"→"**Up**"に変更 ←3つめのポーズ名  
    3つのポーズ名（ポージングはこれから行う）が決まりました  
    ![016_002_4](https://mubirou.github.io/Blender/introduction/jpg/016_002_4.jpg)  
    ※この段階で各ポーズ毎にアーマチュアを選択→[ポーズモード]に変更→[ポーズ]-[アニメーション]-[キーフレーム挿入]-[キャラクター全体]でキーフレームを打っておくと良い（ポーズ名が勝手に変更される場合があるので要注意）

#### ◆ポージング
1. **Normal**用のポージング（上記でキーフレームを既に打っている場合は不要）
    1. [**Normal**]を選択
    1. フレーム位置が**0**になっているか確認
    1. アーマチュアを選択→[ポーズモード]に変更（ポージングはそのまま）
    1. [ポーズ]-[アニメーション]-[キーフレーム挿入]-[キャラクター全体]を選択  
        （ドープシート上にキーフレームが表示されます）  
        ![016_002_5](https://mubirou.github.io/Blender/introduction/jpg/016_002_5.jpg)
1. **Down**用のポージング
    1. [**Down**]を選択
    1. フレーム位置が**0**になっているか確認
    1. アーマチュアを選択→[ポーズモード]に変更してポージング  
        ![016_002_6](https://mubirou.github.io/Blender/introduction/jpg/016_002_6.jpg)
    1. [ポーズ]-[アニメーション]-[キーフレーム挿入]-[キャラクター全体]を選択  
        （ドープシート上にキーフレームが表示されます）  
1. **Up**用のポージング  
    上記と同じように[**Up**]を選択してポージングを行う  
    ![016_002_7](https://mubirou.github.io/Blender/introduction/jpg/016_002_7.jpg)
1. [**Normal**][**Down**][**Up**]と切り替えてみて、想定通りポージングが出来ているか確認する

※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/016_002.blend)  
※Unityでの作業は[こちら](https://github.com/mubirou/Unity/tree/master/introduction#016)を参考  

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
作成日：2019年01月17日


<a name="016_003"></a>
### 003 Unity Humanoid用モデリング

#### ◆モデリングとアーマチュアの関連付け

1. オブジェクトとアーマチュアを関連付ける  
    ![016_003_1](https://mubirou.github.io/Blender/introduction/jpg/016_003_1.jpg)
1. つま先もボーンをつける  
    ![016_003_3](https://mubirou.github.io/Blender/introduction/jpg/016_003_3.jpg)
1. Unityの[Humanoid]に合わせてボーン名を変更する（ボーン名は次の通り）  
    [Hips]-[Spine]-[Chest]-[UpperChest]-[Neck]-[Head]  
    ...[Shoulder.L]-[UpperArm.L]-[LowerArm.L]-[Hand.L]  
    ...[Shoulder.R]-[UpperArm.R]-[LowerArm.R]-[Hand.R]  
    ...[UpperLeg.L]-[LowerLeg.L]-[Foot.L]-[Toes.L]  
    ...[UpperLeg.R]-[LowerLeg.R]-[Foot.R]-[Toes.R]  
    ![016_003_2](https://mubirou.github.io/Blender/introduction/jpg/016_003_2.jpg)
* 注意点
    * ボーンの作成は[Hips]から行う
    * [UpperLeg.L]→[Hips]の順序で選択後、[アーマチュア]-[親]-[作成]-[オフセットを保持]してペアリングする

#### ◆FBXエクスポートの準備①

1. [オブジェクトモード]で[アーマチュア]を選択
1. [ビュー]-[プロパティ]を開く
1. [トランスフォーム]-[回転]を調整
    * X：**-90**°
    * Y：0°
    * Z：0°
1. [オブジェクト]-[適用]-[回転]を選択  
    ※上記のXの値が0になる
1. [トランスフォーム]-[位置]を調整
    * X：0.00000
    * Y：0.00000
    * Z：**0.00000**

#### ◆FBXエクスポートの準備②

1. 引き続き[アーマチュア]を選択した状態で[トランスフォーム]-[回転]を調整
    * X：**90**°
    * Y：0°
    * Z：**180**°

#### ◆FBXエクスポートの準備③

1. [オブジェクト]を選択（オブジェクトモード）  
    ※[回転]のXの値が **-90**° になっているのを確認
1. [オブジェクト]-[適用]-[回転]を選択  
    ※上記のXの値が **0**° になる

#### ◆FBXエクスポートの最終確認

1. 正面（フロント）から見た状態で後ろ向きに立っている状態であること
1. [アーマチュア]（オブジェクトモード）-[トランスフォーム]-[回転]の値を確認
    * X：**90**°
    * Y：**0**°
    * Z：**180**°
1. [オブジェクト]（オブジェクトモード）-[トランスフォーム]-[回転]の値を確認
    * X：**0**°
    * Y：**0**°
    * Z：**0**°
…上記の通りになっていればエクスポートの準備完了  

※ここまでの参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/016_003_1.blend)  

#### ◆FBXエクスポート

1. [ファイル]-[エクスポート]-[FBX（.fbx）]を選択
1. [FBXをエクスポート]設定で[アーマチュア][メッシュ]のみ選択  

※Unity上での続きは[こちら](https://github.com/mubirou/Unity/tree/master/introduction#017)  
※参考ファイル（.blend）は[こちら](https://mubirou.github.io/Blender/introduction/blend/016_003_2.blend)  

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
作成日：2019年01月22日


© 2018-2019 夢寐郎