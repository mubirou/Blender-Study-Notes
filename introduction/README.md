<a name="TOP"></a>

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
|**014**|[テクニック･ヒント1](#テクニック･ヒント1)|参考：[『Blender モデリング･マスター』](#『モデリングマスター』)|[●](#テクニック･ヒント1)|[●](https://amzn.to/2A2595W)|
|**015**|[テクニック･ヒント2](#テクニック･ヒント2)|参考：[『Blender CGイラストテクニック』](#『CGイラストテクニック』)|[●](#テクニック･ヒント2)|[●](https://amzn.to/2HUNroF)|
|016|[テクニック･ヒント3](#テクニック･ヒント3)|参考：アニメーション関連書籍（[●](#『はじめてのBlender』)[●](#『ブレンダーからはじめよう!』)）|[●](#テクニック･ヒント3)|[●](https://amzn.to/2JiTi70)[●](https://amzn.to/2vzog2t)|
***


<a name="インストール"></a>
# <b>001 インストール</b>

1. https://www.blender.org/ にアクセス
1. [Download Blender] → [Download Blender 3.0] を選択→ダウンロード開始
1. ダウンロードされた圧縮ファイル（XXX-linux64.tar.xz）を解凍→展開  
    （Windowsの場合、blender-X.X.X-windows-x64.msi）
1. 展開したフォルダ内の [blender] アイコンをダブルクリック→起動（Windowsの場合[スタート]から）
1. 設定の変更
    1. [Edit（編集）]-[Preferences（プリファレンス）]-[Interface（インターフェイス）]-[Translation（翻訳）] を次の通りに設定
        * Language（言語）：Japanese（日本語）
        * ツールチップ：✔
        * インターフェイス：✔
        * 新規データ：✔
    1. 引き続き [テキストレンダリング] のフォントを次の通りにする（Windowsはデフォルトのまま）  
        * UI用フォント：/usr/share/fonts/opentype/noto/NotoSansCJK-Regular.ttc  
        * 等幅フォント：（空白）←設定によってはPythonコンソールで不具合が生じる（要調査）  
        
    1. [Blenberプリファレンス] 画面の左したの [≡]→[プリファレンスを保存] で設定を保存

実行環境：Blender 2.83.0（Ubuntu 18.04.4 LTS）、Blender 3.0（Windows 10）   
作成者：夢寐郎  
作成日：2018年04月18日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[TOP](#TOP)]


<a name="プリミティブ"></a>
# <b>002 プリミティブ</b>

### 作成方法
1. [オブジェクトモード]で[追加]（上部2段目）を選択
1. [メッシュ] の ➀平面 ➁立方体 ➂円 ➃UV球 ➄ICO球 ➅円柱 ➆円錐 ➇トーラス ➈グリッド ➉モンキー の中から選択

### プリミティブ（メッシュ）の種類
1. 平面（Plane）
    * 頂点数4
1. 立方体（Cube）
    * 頂点数8
1. 円（Circle）
    * 辺のみ（色塗りはなし）
    * 頂点数32
1. UV球（UV Sphere）
    * 経度･緯度をポリゴンで分割されている球
    * 頂点数482（見た目は綺麗）
1. ICO球（Ico Sphere）
    * 三角ポリゴンで構成されている球
    * 頂点数42（ポリゴン数は少ない）
1. 円柱（Cylinder）
    * 頂点数64
1. 円錐（Cone）
    * 頂点数33
1. トーラス（Torus）
    * 頂点数576
1. グリッド（Grid）
    * 頂点数100
1. モンキー（Monkey）
    * Suzannu（スザンヌ）というBlenderのマスコットキャラ
    * 頂点数507

![002](https://mubirou.github.io/Blender/introduction/jpg/002.jpg)

実行環境：Blender 2.79b（Ubuntu 16.04.4 LTS）、Blender 3.0.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年04月19日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[TOP](#TOP)]


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
 
実行環境：Blender 2.80、Ubuntu 18.04.3 LTS  
作成者：夢寐郎  
作成日：2018年06月01日  
更新日：2019年10月08日 Ver.2.80 対応


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

|No.|内容|更新日|
|:--|:--|:--:|
|001|[星型](#014_001)|2022-01-08|
|002|[ベベル･面取り](#014_002)|2022-01-08|
|003|[蛇腹](#014_003)|2022-01-08|
|004|[バネ](#014_004)|2022-01-08|
|005|[壁にパイプを結合](#014_005)|2022-01-08|
|006|[歯車](#014_006)|2022-01-08|
|007|[ネジ山](#014_007)|2022-01-08|
|008|[ハート型に掘る](#014_008)|2022-01-09|
|009|[下絵の利用](#014_009)|2020-06-08|
|010|[テキストオブジェクト](#014_010)|2020-06-04|
|011|[パイプ](#014_011)|2020-06-04|
|012|[UFO（エッジのシャープ化）](#014_012)|2020-06-04|


<a name="014_001"></a>
### 001 星型

![014_001](https://mubirou.github.io/Blender/introduction/jpg/014_001.jpg)

1. [追加]-[メッシュ]-[円]
1. 上記を操作したウィンドウの画面左下にある[円を追加]を開き調整
    * 頂点：10（五角星の場合）←**偶数にする**
    * フィルタタイプ：**三角の扇形**
1. [オブジェクトモード]→[編集モード]にする
1. 外周のポイントを１つおきに選択（[shift]+[クリック]を利用）
1. 左側の[スケール]アイコンで星型にする

    ※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_001.blend)

実行環境：Blender 2.83（Ubuntu 18）、Blender 3.0.0（Windows）  
作成者：夢寐郎  
作成日：2018年12月17日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_002"></a>
### 002 ベベル･面取り

![014_002](https://mubirou.github.io/Blender/introduction/jpg/014_002.jpg)

1. [追加]-[メッシュ]-[立方体]を選択
1. 立方体を選択し[編集モード]にする
1. [辺選択]で任意の線を選択（[Shift]+[クリック]で複数選択可）
1. 左側のアイコン群から[ベベル]（上から11個目）を選択
1. 表示された黄色い[●]をドラッグしてベベルを作成
1. 上記を操作したウィンドウの左下に開いた[べべル]を調整（例）
    * 幅：0.5m（0〜∞）
    * セグメント：5（値を大きくすると滑らかになる）
    * シェイプ：0.500（0.000〜1.000）

    ※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_002.blend)

実行環境：Blender 2.83（Ubuntu 18）、Blender 3.0.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月17日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_003"></a>
### 003 蛇腹

![014_003](https://mubirou.github.io/Blender/introduction/jpg/014_003.jpg)

1. [追加]-[メッシュ]-[円柱]
1.  上記を操作したウィンドウの左下にある [円柱を追加] を開き調整（例）
    * 深度：3m
    * ふたのフィルタタイプ：なし
1. [オブジェクトモード]→[編集モード] にする
1. 左側のアイコン群の中から [ループカット]（上から13個目）を選択
1. ループカットしたい面でとりあえず左クリック
1. 上記を操作したウィンドウの左下に開いた[ループカットとスライド]を調整（例）  
    * 分割数：17 ←奇数にする
1. 以下の状態にしてから次の作業を行う  
    * 左側のアイコン群の一番上 [ボックス選択] を選ぶ
    * [ビュー]-[視点]-[前] にする
    * [ビュー]-[透視/平行投影] で「平行投影」にする
    * 右上のアイコン群から [透過表示を切替え]（右から5番目）を選択し「透過表示」にする
1. [矩形で範囲指定](#ショートカットキー)で1本おきにループ状に [shift] キーを押しながら選択
1. 左側のアイコン群の中から [スケール]（上から5個目）を選択
1. 3Dマニュピレーターの中央の白い輪をドラッグして縮小（要注意）  
    （Shiftキーを押しながら行うと微調整可能）
1. 上記を操作したウィンドウの左下に開いた[拡大縮小]を調整  
        * X：0.800（任意）  
        * Y：0.800（任意）  
        * Z：1.000 ←重要  
    （面を張る場合は、頂点群を選択→[面]-[フィル]を選択）

    ※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_003.blend)

実行環境：Blender 2.83（Ubuntu 18）、Blender 3.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月18日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_004"></a>
### 004 バネ

![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_2.jpg)

1. [追加]-[メッシュ]-[円]
1. 上記を操作したウィンドウの左下に開いた [円を追加] を調整
    * 頂点：12
    * 半径：0.2m
    * 回転（X）：90°
1. [オブジェクト]-[適用]-[回転] ←回転した状態をデフォルトとして適用（重要）  
    * 3D ビューの右端に隠れている [アイテム]-[トランスフォーム]-[回転]-[X] の値が90°→0°になる
1. [オブジェクトモード]→[編集モード] にする
1. 円の[トランスフォーム]-[中心]-[X]を0m→-0.5mに変更
1. [編集モード]→[オブジェクトモード] に変更
1. [Shift]+[S] で [カーソル→ワールド原点] を選択（3Dカーソルの位置を原点に移動）にして、(0,0,0)の位置に [追加]-[エンプティ]-[十字] で空のオブジェクトを作成（名前を "エンプティ_バネ用" に変更）
1. 円のオブジェクトを選択して [オブジェクトモード]→[編集モード] に変更
1. 円を選択した状態で、右側のスパナ
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    タブを選択→[モディファイアーを追加]-[生成]-[スクリュー] を選択し各種設定  
    * 軸オブジェクト：エンプティ_バネ用（上記で作成）
    * スクリュー：0.5m
    * 反復：5
1. 再び [編集モード]→[オブジェクトモード] に変更
1. ①円と②エンプティを選択
1. [オブジェクト]-[ペアレント]-[オブジェクト] を選択し次の通りに設定
    * タイプ：オブジェクト
    * トランスフォーム維持：✔
1. [シーンコレクション] 内で "円" と "エンプティ_バネ用" にネスト化されたのを確認

    ※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_004.blend)

実行環境：Blender 2.83（Ubuntu 18）、Blender 3.0.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月19日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_005"></a>
### 005 壁にパイプを結合

![014_005_1](https://mubirou.github.io/Blender/introduction/jpg/014_005_1.jpg)

#### ◆平面を作成
1. [追加]-[メッシュ]-[平面]
1. 上記を操作したウィンドウの左下に開いた [平面を追加] を調整
    * 回転（X）：90°

#### ◆パイプを作成
1. [追加]-[メッシュ]-[円柱]
1. 上記を操作したウィンドウの左下に開いた [円柱を追加] を調整
    * 頂点：8
    * 半径：0.2m
    * 深度：2m
    * 位置（Y）：-1.1m
    * 回転（X）：90°

### ◆平面とパイプを１つのオブジェクトにする
1. 上記の平面と円柱を両方選択
1. [オブエジェクト]-[結合]（重要）
1. [オブジェクトモード]→[編集モード] にする

    ![014_005_2](https://mubirou.github.io/Blender/introduction/jpg/014_005_2.jpg)

#### ◆穴をあける
1. [ビュー]-[視点]-[前] に変更
1. 平面を選択した状態で、左側のアイコン群の中から [ループカット] を選択（上から13個目）
1. ループカットする平面でとりあえず左クリック
1. 上記を操作したウィンドウの左下にある [ループカットとスライド] を開き調整（例）  
    * 分割数：2
1. 縦方向にもも上記と同様の方法を行う
1. 更に縦横中央に1本ずつ十字にカット
1. [拡大縮小](#ショートカットキー) 等でサイズを調整
1. [面選択] を使って穴をあける
1. [頂点選択] を使って穴を形をパイプに近づける（図はフロント･並行投影）

    ![014_005_3](https://mubirou.github.io/Blender/introduction/jpg/014_005_3.jpg)

#### ◆穴の部分を結合
1. 平面および円柱で、[頂点選択] を使って結合したいところ全て選択
1. [辺]-[辺ループのブリッジ] で結合 ←1つ1つ面を作るより早い

    ![014_005_4](https://mubirou.github.io/Blender/introduction/jpg/014_005_4.jpg)

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_005.blend)

実行環境：Blender 2.83（Ubuntu 18）、Blender 3.0.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月19日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_006"></a>
### 006 歯車

![014_006_1](https://mubirou.github.io/Blender/introduction/jpg/014_006_1.jpg)

#### ◆歯車を作成
1. [追加]-[メッシュ]-[円]
1. 上記を操作したウィンドウの左下に開いた [円を追加] を調整
    * 頂点：32 ←偶数にする
    * フィルタイプ：なし
1. [オブジェクトモード]→[編集モード] にする
1. 外周のポイントを１つおきに選択（[Shift]+[クリック]を利用）
1. [拡大･縮小](#ショートカットキー) で星型にする
1. 全てを選択した状態で [メッシュ]-[複製]→そのまま [右クリック] で確定
1. 左側のアイコン群の中から [回転]（上から4番目）を選び少し回転  
    ![014_006_2](https://mubirou.github.io/Blender/introduction/jpg/014_006_2.jpg)
1. 上記を操作したウィンドウの左下に開いた [回転] で微調整（任意）
1. 全てを選択（Aキー）した状態で [メッシュ]-[削除]-[辺と面のみ] を選択（頂点のみ残る）
1. 全てを選択（Aキー）した状態で [頂点]-[頂点から新規辺/面作成]
1. [面選択]で面を選択して左側の[押し出し]アイコン（上から10個目）で厚みを付ける

#### ◆穴をあける（ブーリアン）
1. [編集モード]→[オブジェクトモード] にする
1. [追加]-[メッシュ]-[円柱] で穴をあけるためのオブジェクトを作成（後に削除）
1. [スケール](上から5個目) で穴のサイズを決める  
    ![014_006_3](https://mubirou.github.io/Blender/introduction/jpg/014_006_3.jpg)
1. 上記の"歯車のみを選択"した状態でスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[生成]-[ブーリアン] を選択し各種設定
    * 演算：差分
    * オブジェクト：円柱 ←上記で作成したもの
1. [シーンコレクション] のツリーで上記の円柱を見えなくする

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_006.blend)

実行環境：Blender 2.8（Ubuntu 18）、Blender 3.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月20日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_007"></a>
### 007 ネジ山

![014_007_1](https://mubirou.github.io/Blender/introduction/jpg/014_007_1.jpg)

#### ◆ネジの頭部を作成
1. [追加]-[メッシュ]-[UV球]
1. 上記を操作したウィンドウの左下に開いた [UV球を追加] で調整
    * セグメント：16
    * リング：24
1. [編集モード] で（重要）上下につぶし半分を削除
1. 下部に面を張るため、頂点群を選択→[面]-[フィル] を選択

#### ◆十字の凹み部分を作成
1. [オブジェクトモード] で新たに [立方体] を作成
1. [オブジェクト]-[オブジェクトの複製]→90°回転して十字型にする  
    ![014_007_2](https://mubirou.github.io/Blender/introduction/jpg/014_007_2.jpg)

#### ◆ネジを凹ます
1. [オブジェクトモード]でネジの頭部のみ選択
1. スパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[ブーリアン]を選択し各種設定
    * 演算：差分
    * オブジェクト：立方体（上記で作成した十字型のうち縦横どちらか）
1. 同様に十字型の残り1つ使ってブーリアン処理する
1. 不要になった立方体2つを[[シーンコレクション] のツリーで見えなくする

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_007.blend)

実行環境：Blender 2.8（Ubuntu 18）、Blender 3.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月21日  
更新日：2022年01月08日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_008"></a>
### 008 ハート型に掘る

![014_008_1](https://mubirou.github.io/Blender/introduction/jpg/014_008_1.jpg)

1. [追加]-[メッシュ]-[UV球]
1. [オブジェクトモード]→[編集モード] にする
1. [ビュー]-[視点]-[前]にして[並行投影] にする
1. [選択]-[なし] で選択を全て解除
1. 左側のアイコン群から [ナイフ] アイコン（上から14番目）を選択
1. 左クリックを繰返しながらハート型を作成
1. 終点（始点と同じ）でクリック直後 [Enter] キーを押す ←わかりにくい  
    ![014_008_2](https://mubirou.github.io/Blender/introduction/jpg/014_008_2.jpg)
1. [面選択] でハート全体を選択
1. [押し出し] アイコン（上から10番目)で凹ます
1. 凹みのメッシュを平坦にしたい場合は [拡大縮小] で平らにする（次の方法を使うと便利）
    * [ビュー]-[視点]-[右] する
    * [ワイヤーフレーム] にする
    * [シーン全体を透過表示します] ボタンを選択
    * 画面左側のアイコン群から [拡大縮小] を選択し調整
        * X: **1.000**
        * Y: **0.000**
        * Z: **1.000**

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_008.blend)

実行環境：Blender 2.83（Ubuntu 18）、Blender 3.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月21日  
更新日：2022年01月09日 Ver.3.0.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_009"></a>
### 009 下絵の利用

![014_009_1](https://mubirou.github.io/Blender/introduction/jpg/014_009_1.jpg)

#### ◆下絵の用意
1. 方眼罫ノートなどを利用して「正面」と「右横」から見たイラストを作成
1. 上記のイラストを画像としてデスクトップ上に .png または .jpg ファイルで保存  
    ![014_009_2](https://mubirou.github.io/Blender/introduction/jpg/014_009_2.jpg)

#### ◆下絵の読込み
1. [ビュー]-[エリア]-[四分割表示]にする
1. 上記の下絵を[フロント･平行投影]にドラッグ＆ドロップ
1. [シーンコレクション]上で読み込んだ画像を選択して複製
1. [トップ･平行投影]で片方の画像を90°回転
1. 右側のアイコン群のオブジェクトデータプロパティ
![014_009_4](https://mubirou.github.io/Blender/introduction/jpg/014_009_4.jpg)
タブを選び両方の画像の[不透明度]を[0.200]にする
1. [移動]アイコンで正面と横からのイラストが重なるように調整  
    ![014_009_3](https://mubirou.github.io/Blender/introduction/jpg/014_009_3.jpg)
1. 両方の画像は選択ができないようにロックする [[参考サイト](https://tamago-design.net/lock-01)]

#### ◆モデリング
1. 下絵を参考にモデリング
1. モデリング途中の[編集モード]でスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モデファイアーを追加]-[ミラー]を選択し各種設定
    * 軸：X
    * クリッピング：✔ ←鏡像との境界からメッシュがはみ出ないようになる

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/zip/014_009.zip)

参考サイト：[3DCG暮らし](https://tohawork.com/blueprint)  
実行環境：Blender 2.83（Ubuntu 18）、Blender 3.0.0（Windows 10）  
作成者：夢寐郎  
作成日：2018年12月26日  
更新日：2020年06月08日 Ver.2.83.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_010"></a>
### 010 テキストオブジェクト

![014_010](https://mubirou.github.io/Blender/introduction/jpg/014_010.jpg)

#### フォントの用意
1. https://www.1001freefonts.com/ から任意のフォントを選択
1. ダウンロードしたら解凍（**.TTF** や **.otf** ファイルのみ必要 / インストールは不要）

#### テキストオブジェクトの作成
1. [追加]-[テキスト]を選択
1. [オブジェクトモード]→[編集モード]に変更
1. 表示文字を "Text" から任意の文字に変更
1. 右側のアイコンタブの中からの「**a**」アイコンを選択
1. [フォント]-[標準]のフォルダーアイコンから上記の **.TTF** また **.otf** ファイルを指定
1. 引き続き各種設定
    * [シェイプ]-[プレビュー解像度U]：12（1〜64）
    * [ジオメトリ]-[押し出し]：0.1m
    * [ベベル]-[深度]：任意

* [オブジェクトモード]に変更後、[オブジェクト]-[変換]-[メッシュ/テキストからカーブ]や[カーブ/メタ/サーフェス/テキストからメッシュ] で形状の変更が可能 
* カーブに沿って文字を並べることも可能（要調査）

* 参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/zip/014_010.zip)

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2018年12月26日  
更新日：2020年06月04日 Ver.2.83.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_011"></a>
### 011 パイプ

![014_011_1](https://mubirou.github.io/Blender/introduction/jpg/014_011_1.jpg)

#### ◆カーブの作成（いきなり[追加]-[カーブ]で作成してもよい）
1. [追加]-[メッシュ]-[円]や[平面] などを次の機能などを使って編集をしてパイプとなる[頂点]と[辺]で構成されるオブジェクトを以下の機能を使うなどして作成  
    * [オブジェクト]-[統合]
    * [頂点]-[頂点からの新規辺/面]
    * [押し出し](#ショートカットキー) ←頂点の押し出し  
    * [オブジェクト]-[変換]-[カーブ/メタ/サーフェス/テキストからメッシュ] → [編集モード] → [ナイフ]  
    ![014_011_2](https://mubirou.github.io/Blender/introduction/jpg/014_011_2.jpg)
1. [編集モード]→[オブジェクトモード]に変更
1. [オブジェクト]-[変換]で[メッシュ/テキストからカーブ]で「カーブ」に変換

#### ◆カーブをパイプ形状にする
1. [オブジェクトモード]で[プロパティエディタ]-
![014_011_3](https://mubirou.github.io/Blender/introduction/jpg/014_011_3.jpg)
で各種設定
    * [シェイプ]-[フィルモード]：フル
    * [ジオメトリ]-[ベベル]-[深度]：0.2m
    * [ジオメトリ]-[ベベル]-[解像度]：4（0〜32）

#### ◆パイプに厚みを付ける（オプション）
1. [オブジェクトモード]で、[オブジェクト]-[変換]→[カーブ...からメッシュ]に変更
1. [編集モード]にして、右側のスパナ
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    タブを選択→[モディファイアーを追加]-[生成]-[ソリッド化]を選択し設定  
        * 幅：0.05m

#### ◆途中の太さを変更する（オプション）
1. [オブジェクト]-[変換]-[カーブ/メタ/サーフェス/テキストからメッシュ] にする
1. [編集モード]で、左側のアイコン群から[ループカット]（上から12個目）を選択
1. ループカットしたいところで左クリック（2箇所）  
    ![014_011_4](https://mubirou.github.io/Blender/introduction/jpg/014_011_4.jpg)
1. 太くしたい部分を選択した状態で（面選択）、[面]-[法線に沿って面を押し出し]で操作

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_011.blend)

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2018年12月27日  
更新日：2020年06月04日 Ver.2.83.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="014_012"></a>
### 012 UFO（エッジのシャープ化）

![014_012_1](https://mubirou.github.io/Blender/introduction/jpg/014_012_1.jpg)

#### ◆UFOの制作
1. [追加]-[メッシュ]-[円] を選択後調整
    * 頂点：24
    * フィルタイプ：三角の扇形
1. 視点を上にして、[拡大縮小] アイコンを使って拡大
1. 画面右側に開いた[トランスフォーム]-[拡大縮小] で調整
    * X,Y,Z 共に1.600
1. [編集モード] にして（視点は前）、[押し出し](#ショートカットキー) で厚みをつける（0.2m程度）
1. [オブジェクトモード] にして、[追加]-[メッシュ]-[UV球]
1. 左下に開いた [UV球を追加] で調整
    * セグメント：12
    * リング：12
1. 円の厚み分弱、UV球を上に移動
1. UV球を選択し [編集モード] にして半分削除
1. 上記の下部に小さなUV球を4つ追加  
    ![014_012_2](https://mubirou.github.io/Blender/introduction/jpg/014_012_2.jpg)
1. UFOの全てのパーツを選択した状態で [オブジェクト]-[統合]

#### ◆滑らかにする
1. [オブジェクトモード] 状態で、右側のスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[生成]-[サブディビジョンサーフェス] を選択  
        * レンダー：2（初期値2）
        * ビュー：2（初期値1）
1. [オブジェクト]-[スムーズシェード] を選択  
    ![014_012_3](https://mubirou.github.io/Blender/introduction/jpg/014_012_3.jpg)

#### ◆一部をシャープなエッジにする
1. [編集モード] に変更
1. [全選択解除](#ショートカットキー) する
1. [辺選択] でシャープなエッジにしたい [辺] を選択（Ctrl+マウス左ボタン）  
1. 画面右側の [トランスフォーム] で調整
    * 辺データ：平均クリース：1.00  
    ![014_012_4](https://mubirou.github.io/Blender/introduction/jpg/014_012_4.jpg)

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/014_012.blend)

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2019年01月04日  
更新日：2020年06月04日 Ver.2.83.0 対応  
[[テクニックヒント1 TOP](#テクニック･ヒント1)]


<a name="テクニック･ヒント2"></a>
# <b>015 テクニック･ヒント2</b>

|No.|内容|更新日|
|:--|:--|:--:|
|001|[ブロック（エッジの超シャープ化と配列複製）](#015_001)|2020-06-08|
|002|[ワイングラス](#015_002)|2020-06-08|
|003|[額縁](#015_003)|2020-06-08|
|004|[窓（正確なUVマッピング）](#015_004)|2020-06-10|
|005|[サイコロ](#015_005)|2020-06-10|


<a name="015_001"></a>
### 001 ブロック（エッジの超シャープ化と配列複製）

![015_001](https://mubirou.github.io/Blender/introduction/jpg/015_001_1.jpg)

#### ◆ブロックのパーツを作成
1. [追加]-[メッシュ]-[立方体]で立方体を1つ作成
1. [編集モード]に変更
1. 上の面だけ選択して[面]-[面を差し込む]  
    ![015_001_2](https://mubirou.github.io/Blender/introduction/jpg/015_001_2.jpg)
1. 引き続き[面]-[面を押し出し]で上に押し出す
1. [オブジェクトモード]に変更
1. 左側のアイコン群の中からスパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)タブを選択
1. [モディファイアーを追加]-[生成]-[サブディビジョンサーフェス]→各種設定  
        * レンダー：2
        * ビューポート：2（初期値：1）
1. [オブジェクト]-[スムーズシェード]を選択  

#### ◆エッジの超シャープ化
1. [編集モード]に戻す
1. エッジをシャープにしたい辺を選択（Shift+右クリック）  
    ![015_001_3](https://mubirou.github.io/Blender/introduction/jpg/015_001_3.jpg)
1. [N]キーで[トランスフォーム]を表示し調整
    * 辺データ：平均クリース：1.00 
1. シャープさが不足している場合、[ループカット]を使って、分割線をシャープにしたいエッジ部分で重ねます  
    ![015_001_4](https://mubirou.github.io/Blender/introduction/jpg/015_001_4.jpg)

#### ◆配列複製
1. [編集モード]のまま、スパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[生成]-[配列]→各種設定  
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

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/015_001.blend)

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2019年01月06日  
更新日：2020年06月08日 Ver.2.83.0 対応  
[[テクニックヒント2 TOP](#テクニック･ヒント2)]


<a name="015_002"></a>
### 002 ワイングラス

![015_002_1](https://mubirou.github.io/Blender/introduction/jpg/015_002_1.jpg)

#### ◆ドロー系ソフトからの読み込み
1. [Inkscape](https://github.com/mubirou/Inkscape)などでワインの断面を[作成](https://mubirou.github.io/Blender/introduction/svg/wineglass.svg)（プレーンSVGファイル）
1. Blender上で[ファイル]-[インポート]-[ScalableVectorGraphics（.svg）]から上記の.svgファイルをインポート
1. 右側の[シーンコレクション]ウィンドウから上記の.svgファイルを選択
1. 何れかの3Dビューを選択→[N]キーで[トランスフォーム]を表示＆設定
    * 回転（Xのみ）：90°
    * 拡大縮小（X,Y,Z）：10.000

#### ◆カーブの回転体を作る
1. [編集モード]に変更
1. Z軸がワインの中心軸になるように移動  
    ![015_002_2](https://mubirou.github.io/Blender/introduction/jpg/015_002_2.jpg)

1. [編集モード]でスパナアイコン![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[生成]-[スクリュー]→各種設定  
        * 座標軸：Y  

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/015_002.blend)

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2019年01月08日  
更新日：2020年06月08日 Ver.2.83.0 対応  
[[テクニックヒント2 TOP](#テクニック･ヒント2)]


<a name="015_003"></a>
### 003 額縁

![015_003](https://mubirou.github.io/Blender/introduction/jpg/015_003.jpg)

#### ◆ドロー系ソフトからの読み込み
1. [Inkscape](https://github.com/mubirou/Inkscape)などで額縁の断面を[作成](https://mubirou.github.io/Blender/introduction/svg/frameDesign.svg)（プレーンSVGファイル）
1. 同様に額縁のサイズとなる矩形を[作成](https://mubirou.github.io/Blender/introduction/svg/frameSize.svg)（プレーンSVGファイル）
1. Blender上で[ファイル]-[インポート]-[ScalableVectorGraphics（.svg）]から上記の2つの.svgファイルをインポート
1. [オブジェクトモード]でフレームの枠（frameSize.svg）のオブジェクトを選択
1. 右側のアイコンタブ群から
![014_011_3](https://mubirou.github.io/Blender/introduction/jpg/014_011_3.jpg)
を選択→[ジオメトリ]→[ベベル]→[オブジェクト]を上記の額縁の断面のオブジェクトにする
1. [シーンコレクション]から[frameSize.svg]や[frameDesign.svg]を選択し、[拡大縮小]するなどして調整

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/015_003.blend)

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2019年01月08日  
更新日：2020年06月08日 Ver.2.83.0 対応  
[[テクニックヒント2 TOP](#テクニック･ヒント2)]


<a name="015_004"></a>
### 004 窓（正確なUVマッピング）

# この項目は編集中です

![015_004_1](https://mubirou.github.io/Blender/introduction/jpg/015_004_1.jpg)

#### テクスチャの用意
1. テクスチャを用意（[window.png](https://mubirou.github.io/Blender/introduction/png/window.png)）  
    ※テクスチャは[textures.com](https://www.textures.com/)を利用するとよいでしょう
1. [追加]-[メッシュ]-[立方体]で立方体を作成
1. [編集モード]に変更
1. 左側のアイコン群の中から[ループカット]で窓の位置に合わせて分割
1. 何れかの3Dビュー画面左上アイコンから[エディター]タイプを[UVエディター]に変更
1. [面選択]でテクスチャを貼りたい面を選択→[右クリック]
1. 開いた[面コンテクストメニュー]→[面のUV展開]→[展開]
1. 何れかの3Dビュー画面の[3Dビューのシェーディング]を[マテリアルプレビューモードで表示]にします（右上のアイコン）
1. [編集モード]で、テクスチャを貼りたい面を選択している事を確認
1. ![015_004_5](https://mubirou.github.io/Blender/introduction/jpg/015_004_5.jpg)
    アイコンを押し→[新規]を選択
1. マテリアル名を"マテリアル"→"窓"に変更
1. [サーフェス]-[ベースカラー]-[◯]-[テクスチャ]-[画像テクスチャ]を選択
1. [開く]から上記の.pngファイルを選択  
1. [UVエディタ]画面で範囲の変更や角度を調整します  
1. [割り当て]を選択 ←重要
〜以上で窓の面は終了。以下ほかの面の色を設定します〜
1. 他の面を選択
1. ![015_004_5](https://mubirou.github.io/Blender/introduction/jpg/015_004_5.jpg)
    アイコンを押し→[+]→[新規]→[ベースカラー]の色（任意）を変更→[割り当て]

※Unityで利用する場合は.fbxファイルでエクスポートし、テクスチャ（.png）と一緒に（相対的階層を維持したまま）Unityプロジェクトの[Assets]フォルダに保存して下さい

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/zip/015_004.zip)  

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2019年01月09日  
更新日：2020年06月10日 Ver.2.83.0 対応  
[[テクニックヒント2 TOP](#テクニック･ヒント2)]


<a name="015_005"></a>
### 005 サイコロ

![015_005_1](https://mubirou.github.io/Blender/introduction/jpg/015_005_1.jpg) 

1. [展開図](https://mubirou.github.io/Blender/introduction/png/dice.png)を用意
1. [追加]-[メッシュ]-[立方体]で作成
1. [編集モード]に変更
1. 上の展開図を参考に、立方体の上がサイコロの1になるように、辺選択で切れ目（シーム）を選択  
    ![015_005_2](https://mubirou.github.io/Blender/introduction/jpg/015_005_2.jpg)
1. 右クリック→コンテキストメニュー→[シームをマーク]を選択  
    （上記で選択した辺が太いオレンジ色になる
1. [面選択]で立方体の全ての"面"を選択
1. 何れかの画面の[エディタータイプ]を[UVエディター]に変更
1. 何れかの3Dビュー画面の[3Dビューのシェーディング]を[マテリアルプレビューモードで表示]にします（右上のアイコン）
1. ![015_004_5](https://mubirou.github.io/Blender/introduction/jpg/015_004_5.jpg)
    アイコンを押し→[新規]ボタンを選択
1. マテリアル名を、"サイコロ用"にする（任意）
1. [サーフェス]-[ベースカラー]-[◯]-[テクスチャ]-[画像テクスチャ]を選択
1. [開く]から上記の.pngファイルを選択  
1. [UVエディタ]画面で範囲の変更や角度を調整します  
1. [割り当て]を選択 ←重要 

※Unityで利用する場合は.fbxファイルの他、テクスチャ（.png）も必要です

※参考ファイル（.blend）を[ダウンロード](https://mubirou.github.io/Blender/introduction/zip/015_005.zip)  

※実践例（.blend）を[ダウンロード](https://mubirou.github.io/Blender/introduction/zip/015_005_2.zip)  

実行環境：Blender 2.83.0、Ubuntu 18.04.4 LTS  
作成者：夢寐郎  
作成日：2019年01月09日  
更新日：2020年06月10日 Ver.2.83.0 対応  
[[テクニックヒント2 TOP](#テクニック･ヒント2)]


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
1. 円柱から、[ループカット][押し出し][クリース:1.00][ソリッド化]などを使ってモデリング  
    ![016_001_2](https://mubirou.github.io/Blender/introduction/jpg/016_001_2.jpg)  
    ※パーツ毎に作成した場合は[オブジェクト]-[統合]で1つのオブジェクトにする（必要に応じて[適用]をする）  
    ※ウェイト調整がしやすいように広げた状態でモデリングする 
1. [オブジェクトモード]でスパナアイコン
    ![014_004](https://mubirou.github.io/Blender/introduction/jpg/014_004_1.jpg)
    -[モディファイアーを追加]-[サブディビジョンサーフェス]→各種設定  
        * ビュー：2  
        * レンダー：2  
1. [オブジェクト]-[スムーズシェード]を選択

1. [ツール]-[シェーディング]-[スムーズ]を選択   

※ここまでの参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/016_001_1.blend)

#### ◆アーマチュアの作成
1. 上記のオブジェクトを選択し[オブジェクトモード]にする
1. [ワイヤーフレーム表示](#ショートカットキー)にする
1. [追加]-[アーマチュア]を選択  
1. ボーンの関節をモデルの関節に合わせます ←重要  
    ![016_001_3](https://mubirou.github.io/Blender/introduction/jpg/016_001_3.jpg)  
1. 画面右側の![016_001_4](https://mubirou.github.io/Blender/introduction/jpg/016_001_4.jpg)
    タブ（オブジェクトデータプロパティ）を選択→[ビューポート表示]→[最前面]を✔する（ワイヤーフレームでなくてもボーンが見えるようになります）  
    ![016_001_5](https://mubirou.github.io/Blender/introduction/jpg/016_001_5.jpg)
1. 上記で作成した[アーマチュア]を選択した状態で[編集モード]にする
1. ボーンの先端（丸い部分）を選択→[押し出し](#ショートカットキー)→繰り返す  
    ※土台部分にもボーンを伸ばします（Unity上での不具合回避のため）←重要
1. 各ボーンの関節をモデルの関節に合わせます ←重要  
    ![016_001_6](https://mubirou.github.io/Blender/introduction/jpg/016_001_6.jpg)

1. オブジェクトとアーマチュアの関連付け
    1. [オブジェクトモード]で①オブジェクト（スタンドライト）→②アーマチュアの順番に[Shift]キーを押しながら選択
    1. [オブジェクト]-[ペアレント]-[自動のウェイトで]を選択  
    ※親子関係を解除する場合は、オブジェクトとアーマチュアを選択した状態で、[オブジェクト]-[ペアレント]-[親子関係をクリア]を選択

## ＜この項目は現在編集中です＞

#### ◆ウェイトの調整（オプション）
1. 変形のテスト
    1. [オブジェクトモード]でアーマチュアを選択→[ポーズモード]に変更
    1. 任意のボーンを選択し[回転](#ショートカットキー)等で動かしてみる
    1. 不具合を確認（ソケットカバー部分に歪みが生じている）  
        ![016_001_7](https://mubirou.github.io/Blender/introduction/jpg/016_001_7.jpg)
    1. 全てのボーンを選択→[ポーズ]→[トランスフォームをクリア]→[すべて]でポーズを元に戻す（任意）
1. [オブジェクトモード]に戻し、①アーマチュア→②オブジェクト（スタンドライト）の順で両方選択←超重要!!
1. [ウェイトペイント]モードに変更  
（変形のテストをしながらウェイトペイントを行うことが可能になります）
1. [Ctrl]+[マウスの右ボタン]でボーンを選択



1. [編集]-[オブジェクトモードをロック]の✔を外す ←超重要!!
1. [Ctrl]+[マウスの右ボタン]でボーンを選択
1. マウスの右ボタンでボーンを選択→[ツール]-[ブラシ]で影響する範囲を修正（以下注意点）  
    * [ツール]-[ブラシ]を次の通りに設定  
        * ウェイト：1.000 ←真っ赤にする
        * 強さ：1.000
    * マスクを利用する＝ペンマスク用のアイコン
    ![016_001_9](https://mubirou.github.io/Blender/introduction/jpg/016_001_9.jpg)で選択
    * [ワイヤーフレーム](#ショートカットキー)で作業するとわかりやすい  
    ![016_001_8](https://mubirou.github.io/Blender/introduction/jpg/016_001_8.jpg)  

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/016_001_2.blend)

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

※参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/016_002.blend)  
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

※ここまでの参考ファイル（.blend)を[ダウンロード](https://mubirou.github.io/Blender/introduction/blend/016_003_1.blend)  

#### ◆FBXエクスポート

1. [ファイル]-[エクスポート]-[FBX（.fbx）]を選択
1. [FBXをエクスポート]設定で[アーマチュア][メッシュ]のみ選択  

※Unity上での続きは[こちら](https://github.com/mubirou/Unity/tree/master/introduction#017)  
※参考ファイル（.blend)wo(https://mubirou.github.io/Blender/introduction/blend/016_003_2.blend)  

実行環境：Blender 2.79b、Ubuntu 18.0.4 LTS  
作成者：夢寐郎  
作成日：2019年01月22日


© 2018-2019 夢寐郎