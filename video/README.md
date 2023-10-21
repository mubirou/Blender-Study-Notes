# 動画編集<a id="TOP"></a>

### <b>index</b>

[XXXXX](#220X01) | [XXXXX](#220X02)
***


<a name="220X01"></a>
# <b>XXXXX</b>

1. ファイルの用意  
    1. 画像と音声ファイルを用意し任意のフォルダ（SampleFolder）に置く  
    1. Blenderを起動  
    1. 最上段の [ファイル]...[コンポジティング]...の右側に隠れている [＋] から [**ビデオ編集**]-[**ビデオ編集**] を選択  
    1. [ファイル]-[名前をつけて保存] で上記のフォルダ内に **〇〇.blend** として保存  
  SampleFolder  
　  ├ **〇〇.blend**  
　  ├ 〇〇.jpg  
　  └ 〇〇.wav  

1. 編集の準備
    1. 左上の [ファイルブラウザー] 画面のパスを上記のフォルダ（SampleFolder）にする  
    （例）C:\Users\〇〇\Desktop\SampleFolder\
    1. プリンター型アイコンから**出力プロパティ**を開く  
    ![image](https://github.com/mubirou/Blender-Study-Notes/blob/master/video/jpg/202310212147.jpg)  
    1. 各種設定（例）  
        * [フォーマット]-[解像度] など：最終出力の値  
        （注意）中途半端な解像度はＮＧ
        * [フレーム範囲]：最終レンダリング範囲
        * [出力]
            * [パス]：〇〇.mp4 等の出力先
            * [ファイルフォーマット]：FFmpeg 動画
            * [エンコーディング]-[コンテナ]：MPEG-4
            * [動画]-[動画コーデック]：H.264
            * [オーディオ]-[音声コーデック]：MP3

1. 編集
    1. [ファイルブラウザー] のファイルを [ビデオシーケンサー] 上にドラッグ＆ドロップして編集
    1. [終了] フレームを手動で入力（In点･Out点のOut）  
    ![image](https://github.com/mubirou/Blender-Study-Notes/blob/master/video/jpg/202310212209.jpg)  


参考：[カンタン動画入門](https://douga-tec.com/?p=29969)  
実行環境：Blender 3.6.4、Windows 11  
作成者：夢寐郎  
作成日：2023年0X月XX日  


<a name="220X02"></a>
# <b>XXXXX</b>

1. XXXXXX
    * XXXXXX

実行環境：Blender 3.2.1、Windows 10  
作成者：夢寐郎  
作成日：2022年0X月XX日  


© 2022 夢寐郎